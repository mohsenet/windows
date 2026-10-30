[DeepSeek](https://chat.deepseek.com/a/chat/s/0cc6cec0-a7e8-4c0f-bd17-0bdc0a4052d0)


```text
install.wim
install.esd
```

[1]
Insert Windows ISO or bootable windows flash


[2]
Index number of Windows
```bash
DISM /Get-WimInfo /WimFile:X:\sources\install.wim
```

[3]
If install.wim
```bash
DISM /Online /Cleanup-Image /RestoreHealth /Source:WIM:X:\sources\install.wim:1 /LimitAccess
```

[4]
If install.esd
```bash
DISM /Online /Cleanup-Image /RestoreHealth /Source:X:\sources\install.esd /LimitAccess
```

[5]
Finaly
```bash
sfc /scannow
```

