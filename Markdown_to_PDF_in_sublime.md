[https://github.com/segersniels/sublime-markdown-2-pdf](https://github.com/segersniels/sublime-markdown-2-pdf)

过程：
1） 安装[MiKTeX](https://miktex.org/download)
2)  安装[Pandoc](https://github.com/jgm/pandoc/releases/tag/1.19.2.1)
3 )定制sublime text的build system

  3.1）创建一个新的build system（Go to Tools > Build System > New Build System ...）并保存（Sublime Text 3/Packages/User）：
   {  
    "shell_cmd": "pandoc -o \"$file.pdf\" \"$file\" && open -a Preview \"$file.pdf\"",  
    "selector": "text.html.markdown",  
    "path": "C:\\Program Files (x86)\\Pandoc:$PATH"  
  }
  3.2）选择这个新的build system （go back to Tools > Build System and select your new build.）
