# StudentMain Manager
一个专杀极域电子教室的Python程序，具有基于wxPython的GUI。

## 原理
* 使用NTSD调试工具，取得Debug权限后强制结束极域教室（无论极域教室有没有设置任务管理器防杀）。
* 使用微软官方Sysinternals的工具[PsSuspend](https://docs.microsoft.com/zh-cn/sysinternals/downloads/pssuspend)挂起StudentMain进程，可以使得教师端定格画面但不会显示学生端断开。
* 使用IE的全屏模式，将教师端控制屏幕变成一个窗口，可以在进行自己的操作的同时看老师上课。
* 给Windows自带的`sethc.exe`快捷键打补丁，即使不慎被控屏，只需按下5次Shift键即可轻松逃脱控屏。
* 可以配套使用GitHub用户 @快乐的梦鱼 的[JiYuTrainer](https://github.com/imengyu/JiYuTrainer)，取得更好的控制效果。

## 系统要求

* 最低可在Windows XP中使用。在Windows 2000及以下，不能保证程序可以正常打开。

  > 当然了，我觉得各位的电脑再落后也不至于Windows 2000吧。现在主流都是Windows 7了……

## 手动编译

1. 使用`PyInstaller`编译`main.pyw`：

   ```
   pyinstaller --onefile --icon .\image-res\StudentMainManager.ico main.pyw
   ```

2. 将无用的`build`文件夹、`__pycache__`和`main.spec`文件删除。

3. 新建一个文件夹，将`dist`文件夹中的`main.exe`复制过去，改名为`StudentMainManager.exe`。

4. 将`config.ini`、`binaries`文件夹复制过去，即可使用。

## 有关早期版本
本程序的早期版本由我在六年级时使用批处理编写，具有一个文字界面，缺少一些非常基本的功能，比如说保持最前端显示。

由于代码过于粗鄙，这里就不放出来了。

# 使用协议 & 免责声明
若你使用本程序，即认为你已阅读并同意以下条款：
* 本程序仅供学习交流之用途，**禁止将本程序用于任何不道德、不遵守法律的行为**。如果不遵守，产生的后果自负。
* 本程序从你已经了解老师上课的内容的角度出发。如果你希望使用本软件，请务必保证你已经充分了解老师上课的内容。
  如果因为使用本程序而导致对学业成绩的影响，**后果自负**。
* 请遵守本程序的开源协议。

若你不同意以上条款，请**不要使用此程序**。

## 开源许可
Apache-2.0 License（详情请见`/LICENSE`）。
