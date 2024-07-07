# windows

### Create schedule to shutdown with Powershell in windows
```bash
schtasks /create /tn "End of the work" /tr "shutdown -s" /sc ONCE /st "17:15:00"
```
