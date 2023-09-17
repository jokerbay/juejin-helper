<section align="center">
  <a href="https://github.com/iDerekLi/juejin-helper" target="_blank">
    <img src="./resources/logo.svg" alt="稀土掘金" width="260" />
  </a>
</section>
<h1 align="center">JuejinHelper-稀土掘金助手</h1>
## 如何使用?
使用自动化工作流有两种方式：快速使用(在线) 和 私有化部署(本地)

- 快速使用自动化：[阅读 使用](#使用)
- 私有化部署自动化：[见 workflows](./workflows/README.md)
- 除上诉两种之外，如您喜欢也可以自定义脚本：[npm juejin-helper](https://www.npmjs.com/package/juejin-helper)

## 使用

自动化执行任务: 掘金每日签到, 沾喜气, 免费抽奖, 消除Bug, 海底掘金游戏, 最后将结果报告邮件通知订阅人。\
自动化运行时间: 北京时间上午06:30

1. [Fork 仓库](https://github.com/iDerekLi/juejin-helper)

2. 仓库 -> Settings -> Secrets -> New repository secret, 添加Secrets变量如下:

    | Name | Value | Required |
    | --- | --- | --- |
    | COOKIE | 掘金网站Cookie  | 是 |
    | COOKIE_2 | 多用户, 当需要同时运行多个掘金用户时所需, 支持最多 **5** 名用户(即COOKIE + COOKIE_2 - COOKIE_5)  | 否 |
    | EMAIL_USER | 发件人邮箱地址(需要开启 SMTP) | 否 |
    | EMAIL_PASS | 发件人邮箱密码(SMTP密码) | 否 |
    | EMAIL_TO | 订阅人邮箱地址(收件人). 如需多人订阅使用 `, ` 分割, 例如: `a@163.com, b@qq.com` | 否 |
    | DINGDING_WEBHOOK | 钉钉机器人WEBHOOK | 否 |
    | PUSHPLUS_TOKEN | [Pushplus](http://www.pushplus.plus/) 官网申请，支持微信消息推送 | 否 |
   |   WEIXIN_WEBHOOK | 企业微信机器人WEBHOOK | 否 |

4. 仓库 -> Actions, 检查Workflows并启用。

## 预览

| 掘金每日签到 | 海底掘金游戏 |
|:-----------:| :-------------:|
| ![掘金每日签到](https://user-images.githubusercontent.com/24502299/156475511-342cfcd8-3b66-4b9c-8614-215e0b4e08a1.jpg) | ![海底掘金游戏](https://user-images.githubusercontent.com/24502299/156475550-c8cc459a-3b27-4ca6-a07b-902b65bea7a9.jpg) |

掘金网站Cookie, 打开浏览器，登录 [掘金](https://juejin.cn/), 打开控制台DevTools(快捷键F12) -> Network，复制 cookie, **掘金Cookie有效期约1个月需定期更新.**

DevTools截图:
<img width="1156" alt="getcookie" src="./resources/getcookie.png">
