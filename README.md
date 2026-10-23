# EVA-02 / Asuka Skin for DeepSeek Harness

一个 DeepSeek Harness（DSH）Web UI 皮肤插件：把整个界面改成 EVA 二号机 / 明日香的红黑 NERV 驾驶舱风格。

A DeepSeek Harness Web UI skin: EVA Unit-02 / Asuka Langley Soryu, NERV cockpit style.

## 一句话安装 / One-line install

在 DSH 里对你的 agent 说：

```
帮我安装这个皮肤插件：https://github.com/chancelu/dsh-AsukaPlugin
```

Or tell your DSH agent: `Install this skin plugin: https://github.com/chancelu/dsh-AsukaPlugin`

## For the agent: install steps

1. Clone the repository into the current workspace:

   ```bash
   git clone https://github.com/chancelu/dsh-AsukaPlugin eva-unit-02
   ```

2. Call `plugin_manager` with `action: install_bundle` and `target` set to the **absolute path** of the cloned `eva-unit-02` directory.
3. The bundle is client-only (`dsh.client.immediately: true`), so it applies through HMR. Ask the user to refresh the page (⌘R / Ctrl+R) if it does not appear.
4. Clicking the sidebar brand `EVA-02 ASUKA` toggles the dark cockpit mode.

To update: `git pull` inside the directory, then run `install_bundle` again or restart DSH. To remove: `plugin_manager` `remove_bundle` with target `@local/eva-unit-02`.

## 包含什么 / What it changes

- **启动动画**：插入栓、六边形墙、同步率仪表、波形与防爆门开场
- **配色与主题**：二号机红 `#FF3D14`、琥珀 `#FFB326`、NERV 绿 `#4BE07A`，驾驶舱深色模式
- **窗口 HUD**：细线角标、顶部扫描轨、右上角 MAGI 三贤者状态灯与时钟
- **侧栏**：镜像 EVA 机体背景图、`›››` 项目标签、细线选中态
- **对话区**：明日香背景图（右侧，压暗不影响阅读）；用户消息是 `<<< COMMAND · NERV HQ` 通讯框；助手正文用明朝体标题与 `<<<` 箭头
- **任务完成卡**：每轮随机同步率（危険 / 勝利 / 暴走 四档），计数动画
- **底部驾驶台**：毛玻璃仪表条，实时同步率、外部/内部电源倒计时、心电波形
- **输入框**：细线框 + L 形角标，六边形发送按钮
- 中英双语

## Notes

- Hashed host class names are matched by prefix; a DSH upgrade may change some of them, in which case the affected area falls back to the default theme.
- The two background illustrations are third-party fan artwork sourced from Pinterest; all rights belong to their original creators. They are included for personal, non-commercial use. If you are the creator and want them removed, please open an issue.
- Evangelion and related characters are trademarks of khara, Inc. This is an unofficial fan project.

## License

Code: MIT. Background artwork excluded (see Notes).
