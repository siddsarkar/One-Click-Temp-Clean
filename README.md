## OneClickTempClean

> Q: what it does?

> A: This is a batch file which is intended to delete your temporary files with a single click to save time and release memory. The folder it deletes are -

```sh
 C:\Windows\Temp
 C:\Windows\prefetch
 C:\Users\your_user_Folder\AppData\Local\Temp
```

> How to use? (Use any of the Option)

- **Option 1** (Don't want to do steps) here's your option-

  1.  Just download the **code.bat** place it anywhere that can come handy, and double click it to delete your temp files when needed.

- **Option 2** (Here's how to set up yourself)

  1. Create a text document by right clicking.
  2. Name **_filename.txt_** to **_filename.bat_** or any name with .bat extension, click yes on the prompt. (make sure extensions are shown)
  3. Then right click and select edit. (It will open up notepad)
  4. Copy the code below and paste it there-
  5. Save it and exit.
  6. Whenever you feel like deleting your temp files just double click **_filename.bat_** it will automatically delete the files that can be deleted.

```bat
set folder="%temp%"
cd /d %folder%
for /F "delims=" %%i in ('dir /b') do (rmdir "%%i" /s/q || del "%%i" /s/q)
set folder="C:\Windows\Temp"
cd /d %folder%
for /F "delims=" %%i in ('dir /b') do (rmdir "%%i" /s/q || del "%%i" /s/q)
set folder="C:\Windows\prefetch"
cd /d %folder%
for /F "delims=" %%i in ('dir /b') do (rmdir "%%i" /s/q || del "%%i" /s/q)
```
