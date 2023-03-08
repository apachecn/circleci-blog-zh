# 开发恐怖故事，第二部分- CircleCI

> 原文：<https://circleci.com/blog/dev-horror-stories-part-ii/>

**来自出版商的说明:**您已经找到了我们的一些旧内容，这些内容可能已经过时和/或不正确。尝试在[我们的文档](https://circleci.com/docs/)或[博客](https://circleci.com/blog/)中搜索最新信息。

* * *

去年万圣节，我们发出呼吁，寻找多年来一直困扰着你的开发者墓穴的故事。

我们玩得很开心，决定再来一次，时间安排得很诡异…

![LeftPadGif.gif](img/9832c7cbbd74ece27285a6bd5769c6ee.png)请继续阅读那些让你彻夜难眠的令人毛骨悚然的开发故事:

“在我上一份工作中，您的新密码不能包含(作为子串)您之前的 5 个密码中的任何一个。所以他们被要求存储所有明文，以确保这一点。”

“我的公司决定下一步从 om 切换到 React，所以现在我们的前端有三个框架”

“我们需要硬件进行测试。我们负担不起。把它运出去，看看会发生什么。我们可能永远也不会理解不开心的顾客。”

“时间戳仅在本地时间。祝夏令时和凌晨 2 点的活动顺利。”

“…如果已经有一个名为 something 的列，例如“生日”，而这个人(创建数据库的人)想要使用同名的列，而不是重用已经存在的列并用正确的数据填充它，他将创建一个名为“BirtthDate”的列"

我:“嗨，只是写信告诉你，当给定有效数据时，新的 API 将返回一个 500 错误和“ok”消息，并且当请求时，数据随后出现在列表中，好像它都工作正常……”他们:“是的，这是预期的，只需将 500 错误和“OK”消息映射，就好像它是一个 200“Me”:……..达福克”

”在前端做了修改的卡片说道。有些棱角分明，有些自举，有些余烬，当然还有 knockout # its not clutterits polyglot”

"创业:希望我成为 fullstack +dba +项目经理+测试+ GUI 设计师+ scrum master . "

“…必须在我的 jdbc 格式的连接字符串中对我的密码进行 urlencode，然后必须对其进行 base64 编码，并通过一些替换将其放在 yaml 文件中，以便它可以编译为 json，并且不会由于特殊字符而被错误地转义…”

“自制的 SQL Server 加密插件有时会破坏客户数据，而这些数据是生死攸关的。无法重新编译插件。发现导致使用回退密钥的竞争情况。教技术支持用后备密钥解密。浏览编译过的机器码。发现由特定的双字节操作码序列触发的竞争条件，该操作码序列碰巧是可读的 ASCII 码并且是唯一的。教导技术支持人员在 DLL 中使用 Notepad++搜索并替换该操作码序列，将逗号更改为波浪号，从而一劳永逸地解决问题。”