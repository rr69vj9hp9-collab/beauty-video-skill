# 美妆视频 Codex Skill

这是一个用于 Codex 的竖版美妆、护肤产品演示视频剪辑 skill。它强调：

- 以口播为剪辑主时间线
- 删除无口播区间、口误、重复词句和重复拍摄
- 画面与口播共用同一份剪辑清单，避免累计音画漂移
- 默认 1080×1920、30 fps、画面和口播 1.2×
- 可爱手写中文字幕、纯黑描边、无阴影
- 只使用直切
- 产品信息型竖版封面
- 固定背景音乐工作流

## 安装

把仓库克隆到 Codex 的 skills 目录，并保持文件夹名为 `beauty-video`：

```bash
git clone https://github.com/rr69vj9hp9-collab/beauty-video-skill.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/beauty-video"
```

安装后可在 Codex 中直接调用：

```text
用 $beauty-video 剪辑这条护肤产品口播视频
```

## 素材说明

为避免泄露个人信息或公开分发未经授权的媒体文件，本仓库不包含：

- 用户本人或产品的参考截图
- 原始视频
- `Memorable Trip` 音乐文件

请仅把你拥有使用权的图片和音频放到本地的 `assets/` 目录。skill 默认查找：

```text
assets/
|-- caption-reference.jpg
|-- cover-reference.jpg
|-- final-caption-reference.jpg
|-- final-cover-reference.jpg
|-- sequence-reference.jpg
`-- memorable-trip.mp3
```

这些媒体文件已被 `.gitignore` 排除，避免误推送到公开仓库。

## 环境

推荐使用支持 H.264、AAC、libass 和 libfreetype 的 FFmpeg，并安装 Hannotate SC、Yuppy SC 等中文圆润手写字体。

## 授权

本仓库暂未附加开源许可证。若要允许他人复制、修改或再发布，请根据你的意图添加 MIT、Apache-2.0 等许可证。
