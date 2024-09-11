# Errors
This project is riddled with errors. Please fix all the bugs!

## Setup
Use this Guided Project template to create a new repository (see [GitHub-with-CLion](https://github.com/uvmcs120s2021/GitHub-with-CLion) repo for directions).
**Your repository must be named with the convention: Errors-netid**, where netid is your UVM NetID username.

When you first put it into CLion, the Build and Run buttons will be grayed out and unclickable. This is intentional. You will need to start fixing bugs before these buttons can be used.

Remember to commit and push frequently.

## Errors
There are three types of errors:
1. **Compiler errors** prevent your program from running. These are typically CMake or syntax errors.
1. **Runtime errors** occur while the program is running and prevent an exit code of zero. Examples of this include a non-zero exit code and an infinite loop.
1. **Logic errors** are when your program runs to completion (with exit code zero) but does not behave the way you intended. The best way to catch logic errors is through extensive testing and/or the use of the debugger.

For this project, you have been given a very broken program and it is your job to fix it. For each error you fix, log it in the table below.

## Logging Errors
Every time you fix a bug, log it in the README file here:

| Type of error (compiler, runtime, logic) | File | Description | Fix |
| ---------------------------------------- | ---- | ----------- | --- |
| Compiler | CMakeLists.txt | "project Errors called with incorrect number of arguments" | Added the project name to line 2 |
| Compiler | main.cpp       | "multiple calls of functions from spie error"              | changed spie.cpp to spie.h in main |
| Compiler | main.cpp       | "expected ';' before '}' token"                            | added semi colon to return 0 at end of main |
| Compiler | main.cpp       | "switch statement syntax error"                            | added a { and fixed the spacing |
| Compiler | main.cpp       | "request from member 'print_rules' in 'game'"              | took away the () by the game definition |
| Compiler | main.cpp       | "fixed the if else statement on line 47 of main"           | fixed the curly brackets on the statement |
| Compiler | spie.cpp       | "expected unqualified-id before ')' token SPIE_Game()"     | added SPIE_Game:: infrount of the contructor definition |
| Compiler | spie.h         | "ostream has not been declared static char error"          | added std:: to get_player_choice first argument |
| Compiler | spie.h         | "iostream has not been declared static char error"         | added std:: to get_player_choice second argument |
| Compiler | spie.h         | "invalid us of vector template"                            | defined the vector to be for integers |
| Compiler | spie.cpp       | "not returning player choice                               | added return for choice |
| Run time | spie.cpp       | "indexes out of array when a winning number matches an already existing one | changed i = -1 to i = 0 |
| Logic    | spie.cpp       | "Fixed the user input so that letters input are read properly" | changed the while loop condition |
| Logic    | spie.cpp       | "the winning numbers were not being added to the vector    | by looking at the vector in the debugger the values were never added to the vector so i added a line to add them |
| Logic    | main.cpp       | "missing break statment after case p in switch statments"  | added a break statment to line 23 |
| Logic    | main.cpp       | "plays a round if you ask for info"                        | added an over arching if to skip the game if choice = i |





## Grading
This project is due on Gradescope by 11:59pm ET on Friday, February 19th.

### Grading Rubric
- [ ] (2 pts) Fix at least one CMake compiler error (not including the one already given).
- [ ] (2 pts) Fix at least one other compiler error.
- [ ] (3 pts) Fix at least one runtime error.
- [ ] (3 pts) Fix at least one logic error.
- [ ] (4 pts) The README table is populated fully and correctly.
- [ ] (4 pts) Fix at least 15 errors total (note: errors you create do not count).
- [ ] (2 pts) At least one fix description includes debugger usage.
