# Mokugyo 电子木鱼SaaS版

这是一个提交表单即可自动增长功德的SaaS版电子木鱼.

告诉他你是谁, 你想将木鱼送给谁, 以及一段祝福, 木鱼就会为他自动增长赛博功德.

## 为什么要做这个?

赛博木鱼是一个好的概念, 但是其存在痛点: 传统的电子木鱼没有署名, 也没有祝福, 机甲佛祖并不知道需要将功德赠送给谁, 以及如何更好的祝福他.

这个SaaS版电子木鱼可以轻松的告诉机甲佛祖你是谁, 你想将功德送给谁, 以及一段祝福.

Mokugyo的设计之初是希望送给他人木鱼, 当然, 你也可以送给自己.

## 如何使用?

[送给地球的电子木鱼示例页面](https://mokugyo.wofbi1.cn/)

请在Issue中提供给我如下内容:

1. 你的昵称
2. 木鱼接收者的昵称
3. 一段祝福

我就会为你创建一个电子木鱼, 持续的为你增长赛博功德.

当然, 你也可以送给自己木鱼.

## 如何部署?

这是一个Springboot项目, 首先需要你修改`application.properties`中管理员的用户名和密码, 然后你可以直接使用gradle进行打包, 然后使用`java -jar`命令运行.

```shell
# 1. 打包
./gradlew build
# 2. 使用Java21运行
java -jar build/libs/mokugyo.jar
```

随后, 你可访问`http://localhost:36688`查看效果, 你应该可以看到一个给地球的木鱼.

而在`http://localhost:36688/page/manage`中, 你可以管理所有的木鱼.

注意, mokugyo会在`~/`目录下创建数据库文件, 如果你使用root用户运行, 请注意权限问题.

# 信息

1. 木鱼页面是借用了[@Lei钟意](https://leixf.cn/)的[木鱼](https://fish.leixf.cn/), 做出了一些调整. 已经取得作者授权.