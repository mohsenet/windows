
Change time
```powershell
Set-Date -Date "12:54:24"
```

Recommended Approach for Domain Environments
```powershell
# Force resynchronization with the domain time source
w32tm /resync
```
