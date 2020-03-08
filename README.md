# VScode-WSL-CodeRunner
![错误图示](https://github.com/FieldLDQ/VScode-WSL-CodeRunner/blob/master/1.jpg)

VScode中使用WSL作为终端时插件CodeRunner路径错误的解决方法
此种错误是因为插件CodeRunner缺少了判断WSL，保留了Windows地址的反斜杠。我们在codeManager代码中加入一个判断，将反斜杠改为正斜杠。

![修改代码](https://github.com/FieldLDQ/VScode-WSL-CodeRunner/blob/master/2.jpg)

code: 

     else if (windowsShell && windowsShell.toLowerCase().indexOf("wsl") > -1) {
    		  command = command.replace(/([A-Za-z]):/g, this.replacer).replace(/\\/g,"/")
  	  }
			
保存后重启VScode，再次以WSL为终端运行代码

![成功更改](https://github.com/FieldLDQ/VScode-WSL-CodeRunner/blob/master/3.jpg)
