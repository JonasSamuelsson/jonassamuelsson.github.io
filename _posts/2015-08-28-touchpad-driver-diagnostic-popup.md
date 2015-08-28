After installing win 10 & vs2015 I have been getting a popup from TouchPad Driver Diagnostic every time I hit Shift+Alt+L.
Fortunately this can be disabled

1. Open the comamnd prompt with admin privileges
2. Type '```reg add HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\services\SynTP\Parameters\Debug /v DumpKernel /d 00000000 /t REG_DWORD /f```' and hit Enter.