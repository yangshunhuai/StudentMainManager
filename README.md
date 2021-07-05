# StudentMain Manager
一个专杀极域电子教室的Python程序，具有基于wxPython的GUI。

## 原理
* 使用NTSD调试工具，取得Debug权限后强制结束极域教室（无论极域教室有没有设置任务管理器防杀）。
* 使用微软官方Sysinternals的工具[PsSuspend](https://docs.microsoft.com/zh-cn/sysinternals/downloads/pssuspend)挂起StudentMain进程，可以使得教师端定格画面但不会显示学生端断开。
* 使用IE的全屏模式，将教师端控制屏幕变成一个窗口，可以在进行自己的操作的同时看老师上课。
* 可以配套使用GitHub用户imengyu的[JiYuTrainer](https://github.com/imengyu/JiYuTrainer)，取得更好的控制效果。
