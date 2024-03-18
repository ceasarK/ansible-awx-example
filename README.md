tower-example
=============
## group_vars （全局变量目录）
## role目录
```
files
用来存放由 copy 模块或 script 模块调用的文件。

templates
用来存放 jinjia2 模板，template 模块会自动在此目录中寻找 jinjia2 模板文件。

tasks
此目录应当包含一个 main.yml 文件，用于定义此角色的任务列表，此文件可以使用 include 包含其它的位于此目录的 task文件。

handlers
此目录应当包含一个 main.yml 文件，用于定义此角色中触发条件时执行的动作。

vars
此目录应当包含一个 main.yml 文件，用于定义此角色用到的变量。

defaults
此目录应当包含一个 main.yml 文件，用于为当前角色设定默认变量。这些变量具有所有可用变量中最低的优先级，并且可以很容易地被任何其他变量覆盖。所以生产中我们一般不在这里定义变量

meta
此目录应当包含一个 main.yml 文件，用于定义此角色的元数据信息及其依赖关系。存放角色依赖的位置，比如要安装wordpress，我们需要先安装nginx和php，我们把playbook引用在这里，会优先执行这里的内容```
