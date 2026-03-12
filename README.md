# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
<img width="547" height="109" alt="image" src="https://github.com/user-attachments/assets/dd4e9680-2b52-4f78-b7de-f48fb7670387" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="503" height="65" alt="image" src="https://github.com/user-attachments/assets/e9aa5b87-ef9c-41e0-8641-81e6f8b116e9" />



Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="527" height="107" alt="image" src="https://github.com/user-attachments/assets/c4ada696-9bb0-42c5-8343-0ad9e924bda5" />
<img width="709" height="235" alt="image" src="https://github.com/user-attachments/assets/c32544f3-d422-4ee8-8706-bb5cbfe89c55" />



Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="630" height="37" alt="image" src="https://github.com/user-attachments/assets/5d62945b-e798-4a0e-a980-46d272a04bde" />
<img width="502" height="73" alt="image" src="https://github.com/user-attachments/assets/dbd4497f-83c1-4b42-bf0d-229b89f98a7a" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="600" height="77" alt="image" src="https://github.com/user-attachments/assets/9dad5059-bae6-4aff-8e16-2d5c39985038" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="500" height="155" alt="image" src="https://github.com/user-attachments/assets/07d56702-7450-45f5-87b2-30c9e5bc8cfb" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="502" height="139" alt="image" src="https://github.com/user-attachments/assets/0c343e0d-e58a-45ff-80e3-ae09a2724268" />

List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="503" height="574" alt="image" src="https://github.com/user-attachments/assets/995d96df-88d4-46fe-ba7d-2c3fde816c1f" />

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="549" height="215" alt="image" src="https://github.com/user-attachments/assets/fd740304-e689-4159-b205-1251ee620c10" />
T
## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

@echo off
set name=John
echo Hello, %name%!
pause

## OUTPUT
<img width="469" height="89" alt="image" src="https://github.com/user-attachments/assets/2ab9031d-b9a4-4653-bf64-8da33d0629cf" />

Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause

```

## OUTPUT




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.




## OUTPUT

<img width="564" height="134" alt="image" src="https://github.com/user-attachments/assets/b565b1a1-179b-459f-8a9d-0cf40cb7d81c" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```
##OUTPUT
<img width="538" height="176" alt="image" src="https://github.com/user-attachments/assets/36199eb8-929d-4a3a-8f6a-aec7073edaaa" />

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT

<img width="455" height="63" alt="image" src="https://github.com/user-attachments/assets/7363c1ce-857b-41b6-a122-aba3584d159b" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```
## OUTPUT

<img width="411" height="285" alt="image" src="https://github.com/user-attachments/assets/febfa45b-144b-48bb-ab9c-e7f96c553cf3" />


# RESULT:
The commands/batch files are executed successfully.

