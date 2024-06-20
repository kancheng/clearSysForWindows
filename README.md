# Windows 清除暫存檔

```
@echo off
echo 正在清除系統垃圾檔案中，請稍候......
del /f /s /q %systemdrive%\*.tmp
del /f /s /q %systemdrive%\*._mp
del /f /s /q %systemdrive%\*.log
del /f /s /q %systemdrive%\*.gid
del /f /s /q %systemdrive%\*.chk
del /f /s /q %systemdrive%\*.old
del /f /s /q %systemdrive%\recycled\*.*
del /f /s /q %windir%\*.bak
del /f /s /q %windir%\prefetch\*.*
del /f /q %userprofile%\cookies\*.*
del /f /q %userprofile%\recent\*.*
del /f /s /q "%userprofile%\Local Settings\Temporary Internet Files\*.*"
del /f /s /q "%userprofile%\Local Settings\Temp\*.*"
del /f /s /q "%userprofile%\recent\*.*"
DEL /S /F /Q "%systemroot%\Temp\*.*"
DEL /S /F /Q "%AllUsersProfile%\「開始」功能表\程式集\Windows Messenger.lnk"
RD /S /Q %windir%\temp & md %windir%\temp
RD /S /Q "%userprofile%\Local Settings\Temp"
MD "%userprofile%\Local Settings\Temp"
RD /S /Q "%systemdrive%\Program Files\Temp"
MD "%systemdrive%\Program Files\Temp"
RD /S /Q "%systemdrive%\d"
net user aspnet /delete
cleanmgr /sagerun:99
echo 清除系統垃圾檔案完成！
```

## Reference

- https://wuangus.cc/%E6%95%99%E5%AD%B8%E6%B8%85%E9%99%A4%E9%9B%BB%E8%85%A6%E7%B3%BB%E7%B5%B1%E5%9E%83%E5%9C%BEbat%E6%AA%94%E3%80%8A%E5%8A%A0%E5%BC%B7%E7%89%88%E3%80%8B/

- https://wuangus.cc/%E6%95%99%E5%AD%B8%E5%A6%82%E4%BD%95%E8%A3%BD%E4%BD%9C%E6%B8%85%E9%99%A4%E7%B3%BB%E7%B5%B1%E5%9E%83%E5%9C%BEbat%E6%AA%94%EF%BC%8C%E8%BC%95%E9%AC%86%E5%AD%B8%E6%9C%83%E5%AF%AB%E7%A8%8B%E5%BC%8F/
