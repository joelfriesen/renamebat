@echo off
Setlocal enabledelayedexpansion

Set /p find= What do you want to change in the file names?
Set /p replace= What do you want to change it to?

For %%a in (*.html) Do (
    Set "File=%%~a"
    Ren "%%a" "!File:%find%=%replace%!"
)

Exit
