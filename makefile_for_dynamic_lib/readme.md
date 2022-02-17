## 说明
专门编译动态库
编译选项和链接选项增加“-fPIC -shared ”选项。动态库文件固定命名格式为libxxx.so。

"terminal.integrated.profiles.windows": {
        "PowerShell": {
            "source": "PowerShell",
            "icon": "terminal-powershell"
        },
        "Command Prompt": {
            "path": [
                "${env:windir}\\Sysnative\\cmd.exe",
                "${env:windir}\\System32\\cmd.exe"
            ],
            "args": [],
            "icon": "terminal-cmd"
        },
        "Git-Bash": {
            "path": "E:\\Git\\bin\\bash.exe",
            "args": []
        }
    }
