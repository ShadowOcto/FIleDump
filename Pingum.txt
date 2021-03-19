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


echo @echo off >> .\Servers\%ip%.bat
echo title Pinging %ip% >> .\Servers\%ip%.bat
echo echo. >> .\Servers\%ip%.bat
echo type .\Servers\assets.dll >> .\Servers\%ip%.bat
echo echo. >> .\Servers\%ip%.bat
echo echo. >> .\Servers\%ip%.bat
echo echo Pingum By Shadow :^ >> .\Servers\%ip%.bat
echo :ping >> .\Servers\%ip%.bat
echo ping %ip% -l 65500 >> .\Servers\%ip%.bat
echo goto ping >> .\Servers\%ip%.bat


:ping
echo Pong!
start .\Servers\%ip%.bat
timeout /T %delay% >nul
goto ping
