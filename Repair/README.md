[DeepSeek](https://chat.deepseek.com/a/chat/s/0cc6cec0-a7e8-4c0f-bd17-0bdc0a4052d0)


```text
install.wim
install.esd
```

[]
Insert Windows ISO or bootable windows flash


[]
Index number of Windows
```bash
DISM /Get-WimInfo /WimFile:X:\sources\install.wim
```

[]
If install.wim
```bash
DISM /Online /Cleanup-Image /RestoreHealth /Source:WIM:X:\sources\install.wim:1 /LimitAccess
```

[]
If install.esd
```bash
DISM /Online /Cleanup-Image /RestoreHealth /Source:X:\sources\install.esd /LimitAccess
```

[]
Finaly
```bash
sfc /scannow
```

