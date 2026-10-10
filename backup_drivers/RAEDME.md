
## Backup and restore drives

### Backup drivers
```powershell
dism /online /export-driver /destination:D:\DriverBackup
```


# Restore drivers
```powershell
pnputil /add-driver D:\DriverBackup\*.inf /subdirs /install
```

