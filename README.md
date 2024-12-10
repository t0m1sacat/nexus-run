# nexus-run (Nexus Prover 管理工具)

一个便捷的 Nexus Prover 节点管理工具，提供简单的安装、运行和管理功能。自编译，使用最新的 0.4.2 源代码。

## 特性

- 自动检测并安装依赖
- 支持 AMD64 Linux 和 ARM64 macOS
- 一键安装并启动 Nexus Prover
- Prover ID 管理
- 运行状态监控
- tmux 会话管理

## 快速开始

```bash
curl -O https://raw.githubusercontent.com/qzz0518/nexus-run/refs/heads/main/nexus-manager.sh && chmod +x nexus-manager.sh && ./nexus-manager.sh
```

## 系统要求

- Linux (AMD64) 或 macOS (ARM64)
- 支持 APT 或 YUM 的包管理器（Linux）
- Homebrew（macOS）

## 功能选项

1. 安装并启动 Nexus
2. 查看当前运行状态
3. 查看 Prover ID
4. 设置 Prover ID
5. 停止 Nexus
6. 退出

## 注意事项

- 首次运行时会提示输入 Prover ID，如果没有可以直接回车自动生成 (建议使用网页上的 ID)
- 查看运行状态时请使用关闭终端或者 Ctrl+B 再按 D 的方式退出，不要使用 Ctrl+C
- 程序会自动在后台运行，无需保持终端开启
- 服务器内存至少要有 2G RAM，不然会闪退

## 关于 Prover ID 的说明
如果你想在网页上的看到自己的 POINTS ,点击左下角 My Profile 如下图显示的话，你需要使用网页接口的形式获取并使用你的 localId 才能够显示（这里可能有个坑，如果你在CLI跑可能真的需要这个完整的ID才有效，你使用网页版截取的前8位的可能是无效的）。
<img width="1326" alt="image" src="https://github.com/user-attachments/assets/a2107b55-7f8a-4bc6-bbaa-eb17f0ea927c">

网页浏览器进入 https://beta.nexus.xyz/ ，点击F12，按照下图画红圈的地方进行点击，找最后找到 localId，并复制绿色的部分（复制id不要带双引号），使用并设置为 Prover ID
<img width="1137" alt="image" src="https://github.com/user-attachments/assets/e7d038dd-a940-4681-bd8d-aacd1816b2f3">


或者在F12控制台中，输入如下使用命令,则会显示你的id

```js
console.log(localStorage.getItem('flutter.proverId'));
```
<img width="500" alt="image" src="https://github.com/user-attachments/assets/76b99f8f-bcb4-4a70-bf3d-ff346bf8ccb2">



当前使用CLI随机生成id的形式运行并不代表你跑的积分无效，请保存和备份好你随机生成的id，项目方后续应该会出绑定的步骤。

## 关于作者

- Twitter: [@zerah_eth](https://x.com/zerah_eth)
- Github: [qzz0518/nexus-run](https://github.com/qzz0518/nexus-run)

## 推荐工具

- SOL 回收工具: [SOLBack](https://solback.app/)

## 相关链接

- [Nexus Network](https://nexus.xyz/)
- [Nexus Beta](https://beta.nexus.xyz/)
- [Nexus Client](https://github.com/nexus-xyz/network-api)
