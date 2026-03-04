@echo off

:: Check for administrator rights
net session >nul 2>&1
if %errorLevel% == 0 (
    echo Running with administrator rights...
) else (
    echo Requesting administrator rights...
    powershell -Command "Start-Process '%~f0' -Verb RunAs"
    exit /b
)

:: Backup current hosts file
copy "C:\Windows\System32\drivers\etc\hosts" "C:\Windows\System32\drivers\etc\hosts.backup.%date:~-4%%date:~4,2%%date:~7,2%" >nul

echo.
echo Disabling Spotify Ad entries...

(
echo.
echo # === Disabling ===
echo 0.0.0.0 adeventtracker.spotify.com
echo 0.0.0.0 ads-fa.spotify.com
echo 0.0.0.0 ads-akp.spotify.com
echo 0.0.0.0 ads.spotify.com
echo 0.0.0.0 audio-ak.spotify.com
echo 0.0.0.0 audio-akp.spotify.com
echo 0.0.0.0 analytics.spotify.com
echo 0.0.0.0 analytics-fa.spotify.com
echo 0.0.0.0 eventtracker.spotify.com
echo 0.0.0.0 heads-fa.spotify.com
echo 0.0.0.0 partner.spotify.com
echo 0.0.0.0 spclient.wg.spotify.com/ad
echo 0.0.0.0 spclient.wg.spotify.com/ads
echo 0.0.0.0 upgrade.spotify.com
echo # === Finished ===
) >> "C:\Windows\System32\drivers\etc\hosts"

echo.
echo Hosts file updated successfully!
echo.
echo Close Spotify completely (check Task Manager → end all Spotify processes)
echo Then reopen Spotify. Ads should be blocked or skipped.
echo.
echo To remove this blocker later, run the same script again and choose "Remove".
pause
