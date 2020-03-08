# VScode-WSL-CodeRunner
![错误图示](https://github.com/FieldLDQ/VScode-WSL-CodeRunner/blob/master/1.png)
VScode中使用WSL作为终端时插件CodeRunner路径错误的解决方法
此种错误是因为插件CodeRunner缺少了判断WSL，保留了Windows地址的反斜杠。我们在代码中加入一个判断，将反斜杠改为正斜杠。
