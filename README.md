Danmaqua Telegram Bot
======

将哔哩哔哩直播间的同传弹幕转发至 Telegram 聊天、频道以便阅读/存档。

## How to use

### 直接订阅已有的同传弹幕记录频道

订阅 Telegram 频道 [@danmaqua](https://t.me/danmaqua) 获取最新的同传弹幕记录频道。

如果你有自己搭建的弹幕记录频道，也欢迎提交到这里。

### 运行自己的机器人实例

使用前请保证你的运行环境有 Node.js 12+，并在 Telegram `@BotFather` 申请你自己的机器人。

1. 使用 Git Clone 项目到本地
2. 复制一份 `config.sample.js` 并改名为 `config.js` ，按照文件内注释配置好数据库路径、机器人 Token、管理员等
3. 执行 `npm i` 安装必要的依赖
4. 执行 `npm run bot` 启动机器人

### 配置弹幕转发到群组或频道

同传翻译弹幕的辨别以 `config.js` 内的正则表达式为准，请根据自己的需求进行设定。

运行起来自己的实例之后，打开与机器人的 Telegram 聊天，首次使用需要点击 Start 开始对话。

输入 `/subscribe [B 站房间号] [指定的群组/频道 ID]` ，B 站房间号即直播地址最后的一串 ID 而非用户 ID，指定的群组/频道 ID 为 Telegram 内部保存的一串纯数字 ID，你可能需要使用其它 ID 查询机器人来获取，如果你拥有 Android 手机，可以尝试安装 Nekogram 或其它可信任的第三方 Telegram 客户端，打开群组/频道资料页查看 ID。

如果要取消订阅，输入 `/unsubscribe [指定的群组/频道 ID]` 即可，每个群组/频道只能订阅一个 B 站房间。

使用 `/set_hide_username [指定的群组/频道 ID]` 可以开关隐藏弹幕发送用户名，但不推荐使用，将无法得知弹幕发送者，如果遇到无关翻译的弹幕将无法得知用户 ID 进行屏蔽，最重要的是同传大佬付出大量时间和精力为我们提供直播翻译，至少我们要能记住他们的名字。

使用 `/block_user [要屏蔽的用户 ID] [指定的群组/频道 ID]` 可以屏蔽/取消屏蔽来自于指定用户的弹幕，用户 ID 指 B 站空间中看到的 UID，要快速获取 ID，你可以在机器人转发出来的弹幕中，点击蓝色的用户链接，复制 URL 中的 ID 出来。

## Contact author

Telegram: [@fython](https://t.me/fython)

## Licenses

GPLv3