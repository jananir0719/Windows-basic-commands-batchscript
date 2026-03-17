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
<img width="495" height="115" alt="image" src="https://github.com/user-attachments/assets/aa2f12ed-3d18-4fab-92d1-d49acea53e07" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="526" height="63" alt="image" src="https://github.com/user-attachments/assets/ab655804-ef0a-4ac8-90f3-d7480fbfd92f" />


Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="936" height="143" alt="image" src="https://github.com/user-attachments/assets/1554d1b9-2398-44f0-a248-de178ebfda4d" />
<img width="658" height="243" alt="image" src="https://github.com/user-attachments/assets/6b8f9d88-1dcb-4ccb-91d4-0b52d40fb0c3" />



Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="677" height="137" alt="image" src="https://github.com/user-attachments/assets/acb31ae0-1165-4b34-ba25-b1ea5c20cbbd" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="637" height="90" alt="image" src="https://github.com/user-attachments/assets/ca553d8d-7f85-40cb-8d02-14496beb163a" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="495" height="250" alt="image" src="https://github.com/user-attachments/assets/fcf88a09-960f-4020-a8b0-75f57066a487" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="495" height="250" alt="image" src="https://github.com/user-attachments/assets/547cbdbb-a8f5-4917-9fe7-9e6ce0c6102a" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="544" height="954" alt="image" src="https://github.com/user-attachments/assets/08add036-6b8b-4c24-a8c8-c681391ed316" />

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="938" height="225" alt="image" src="https://github.com/user-attachments/assets/f6faddd8-783f-49aa-9b1e-afa23cecec8a" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```

@echo off

set name=John

echo Hello, %name%!

pause
```







## OUTPUT
<img width="392" height="89" alt="image" src="https://github.com/user-attachments/assets/62db531a-5a10-43ba-b75f-7f05a62a2731" />



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

&nbsp;   echo %number% is an odd number.

) else (

&nbsp;   echo %number% is not an odd number.

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

@echo off

for %%i in (1 2 3 4 5) do (

&nbsp;   echo Number: %%i

)

pause




## OUTPUT

<img width="430" height="199" alt="image" src="https://github.com/user-attachments/assets/4aa84ff6-4745-4fc9-bacc-4a81386d387a" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```

@echo off

if exist sample.txt (

&nbsp;   echo sample.txt exists.

) else (

&nbsp;   echo sample.txt does not exist.

)

pause
```
## OUTPUT
<img width="411" height="60" alt="image" src="https://github.com/user-attachments/assets/99c48b69-1046-41e0-beb8-1301d97bf282" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```

@echo off

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
<img width="431" height="283" alt="image" src="https://github.com/user-attachments/assets/a5421d18-8132-4db6-8af3-4153753a62ad" />



# RESULT:
The commands/batch files are executed successfully.

