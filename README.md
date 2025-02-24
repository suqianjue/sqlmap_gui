# SQLMap 可视化工具

# 工具简介

SQLMap 是一款自动化的 SQL 注入漏洞测试工具，它能帮助安全研究人员、渗透测试员和网络安全专家识别、利用和修复SQL注入漏洞。为了更方便用户操作和理解其工作流程，我们推出了 SQLMap 可视化工具，使得SQLMap的操作更加简单直观，尤其适合没有命令行经验的用户。该工具将 SQLMap 命令行工具进行图形化，提供更加直观、易于操作的界面，让用户可以轻松进行 SQL 注入测试。

## 主要特点

* 🎯 **图形化界面**：告别繁琐的命令行输入，通过可视化的界面进行操作。
* 🚀 **快速扫描**：简单设置，轻松启动扫描，节省您的时间。
* 🛠️ **高级功能**：支持 SQLMap 的所有高级功能，如自定义 payload、数据库信息泄露、Web 应用程序防护绕过等。

## 环境要求

* 🖥️ **操作系统**：Windows
* ⚙️ **Java 版本**：工具用使用java11编译
* 🧑‍💻 **SQLMap**：确保本地已经安装并配置好 SQLMap 工具

## 安装步骤

1. **下载工具**
    前往 [https://github.com/suqianjue/tools/releases](https://github.com/suqianjue/tools/releases) 下载双击运行即可使用。
2. **安装依赖**
    确保您的机器已安装 JDK 1.8+ 版本。可以通过以下命令检查 JDK 版本：

    java -version

## 工具截图
双击jar包打开程序如图所示，会在当前文件夹生成一个config.properties的配置文件
![image](https://github.com/user-attachments/assets/aae3db97-0efa-492f-b71c-58a8b46eebd2)


config.properties文件里面记录的是sqlmap路径和代理信息，可在工具中导入，也可手动填写
![image](https://github.com/user-attachments/assets/89f46e4d-ff91-4498-b669-290600e45180)

文件->导入sqlmap，选择sqlmap文件夹就可以了(不用选择具体文件)
![image](https://github.com/user-attachments/assets/d685fb2c-292c-490e-ad6c-ed798306c085)

设置->代理，可以挂代理，工具自带测试代理是否可用功能
![image](https://github.com/user-attachments/assets/891dbd92-f716-47bc-8376-ab5c02a52d0e)


脚本文件会自动获取sqlmap文件中tamper文件夹，也可以手动添加脚本到里面
![image](https://github.com/user-attachments/assets/6255cf57-2c0b-48a0-819f-1ecd82a7130c)

自定义参数在GET请求下就是sqlmap的 -p id ，POST请求就是sqlmap的 -data id=1，GET/POST请求可在url那一行最左边选
测试级别、风险级别、线程数、库、表、列都可以自定义，还有一些可自选的功能项
选择完后点击预览按钮，则会生成sqlmap语句在预览框中显示，可以自定义调整，修改、删除、添加
然后点击start就是开始运行
**注：必须先点预览，预览框中出现了命令才能点start运行**
![image](https://github.com/user-attachments/assets/83e4b346-4141-4d97-a2c3-0198f49c202a)

关于抓包跑，可直接在burp抓包，复制请求包粘贴到文本框中，在需要测试的地方加上 * 点击start即可
其他地方不需要改，可以选择需要的脚本和一些功能项等等
**注：当预览框和抓包跑文本框都有信息时，优先会运行预览框命令**
![image](https://github.com/user-attachments/assets/3ebf9761-826e-420f-a2db-90433fe2ef12)


