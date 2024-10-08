# VScode Setup

If you dont have GCC installed, download it from here:

https://jmeubank.github.io/tdm-gcc/download/

Download the second option:

![alt text](image-6.png)

1. Open the project inside VScode

2. Install the following extensions:

- C/C++
- C/C++ Extension Pack

3. Open your c code file

![alt text](image.png)

4. Press `Ctrl + Shift + P` to open the command palette

5. Type `Run C/C++ file` and select `Run C/C++ file`

![alt text](image-1.png)

6. Choose the gcc compiler

![alt text](image-2.png)

7. A new folder named `.vscode` will be created in your project directory with the file `tasks.json`

8. Open the file `tasks.json`

![alt text](image-3.png)

9. Add the following strings to the `args` array

```json
"-Wall",
"-Werror",
"--pedantic",
"-std=c90",

The output will look like this:

```json
{
    "tasks": [
        {
            "type": "cppbuild",
            "label": "C/C++: gcc.exe build active file",
            "command": "c:\\TDM-GCC-64\\bin\\gcc.exe",
            "args": [
                "-fdiagnostics-color=always",
                "-Wall",
                "-Werror",
                "--pedantic",
                "-std=c90",
                "-g",
                "${file}",
                "-o",
                "${fileDirname}\\${fileBasenameNoExtension}.exe"
            ],
            "options": {
                "cwd": "c:\\TDM-GCC-64\\bin"
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "detail": "Task generated by Debugger."
        }
    ],
    "version": "2.0.0"
}
```

![alt text](image-4.png)

Dont forget to check, whether the `command` points to the correct GCC compiler

10. Press `Ctrl + S` to save the file

11. Run the code again by clicking on:

![alt text](image-7.png)



# Alternative method:

Download the following extension:

- Code Runner

![alt text](image-8.png)

Click on File -> Preferences -> Settings

Type in the search bar:

executormap

![alt text](image-9.png)

Open the file and add:

-Wall -Werror --pedantic -std=c90

![alt text](image-10.png)

Save the file and go to your c code file

Click on Run code:

![alt text](image-11.png)




# How to enable writing inside terminal for scanf etc.

Type in code runner inside the settings search bar and mark the following options:

![alt text](image-12.png)






