@echo off
title Pingum By Shadow
echo.
type logo.dll
echo.
echo Server Adress:
set /p ip=:
cls
echo Ping Delay:
set /p delay=:
cls


echo @echo off >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo title Pinging %ip% >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo echo. >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo type "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\assets.dll" >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo echo. >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo echo. >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo echo Pingum By Shadow :^ >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo :ping >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo ping %ip% -l 65500 >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
echo goto ping >> "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"


:ping
echo Pong!
start "C:\Users\%USERNAME%\Documents\Program Files (x86)\Pingum\Servers\%ip%.bat"
timeout /T %delay% >nul
goto ping
