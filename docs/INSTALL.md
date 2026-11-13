# 安装糕糕 Codex Pet

## 环境要求
使用支持本地自定义宠物的 Codex 桌面客户端。本包采用兼容 v1 的 8×9 精灵图格式；不同客户端版本的界面入口可能不同。

## Windows 安装
1. 下载 `gaogao-v1.0.0.zip` 并解压。不要直接从压缩包内运行或浏览安装文件。
2. 如果 `%USERPROFILE%\.codex\pets\gaogao` 已存在，先将整个旧 `gaogao` 文件夹复制到 pets 目录以外的位置备份。
3. 将压缩包中的 **gaogao 文件夹**复制到 `%USERPROFILE%\.codex\pets\`。如果 pets 目录不存在，可先创建。
4. 确认最终结构如下，不要多套一层 gaogao 文件夹：

```text
%USERPROFILE%\.codex\pets\
└── gaogao\
    ├── pet.json
    └── spritesheet.webp
```

5. 刷新宠物列表或重启 Codex，然后选择“糕糕”。

`%USERPROFILE%` 是 Windows 用户目录的环境变量占位符，不是需要照抄创建的文件夹名。使用自定义 CODEX_HOME 的用户，应安装到其对应的 `pets/gaogao` 目录。

## 更新与撤销
更新前先备份已有同名目录，仅替换糕糕的文件，不修改其他宠物。撤销首次安装时，先停止使用糕糕，再仅移走 `pets/gaogao` 文件夹；如需恢复旧版，将此前备份的 gaogao 放回原位置。

## 常见问题
- 找不到糕糕：核对目录层级、文件名以及客户端是否支持本地自定义宠物，然后重启客户端。
- 动作错位：确认使用完整原版 spritesheet.webp，未裁切、压缩成有损图片或更改尺寸。
- 工作状态没有跑步：这是正常设计。`running` 表示 Codex 正在执行任务，方向移动由 `running-left` / `running-right` 表示。

## 文件校验
安装包附带 `SHA256SUMS.txt`。可在解压目录用 PowerShell 的 `Get-FileHash .\gaogao\spritesheet.webp -Algorithm SHA256` 查看哈希，并与校验文件对应条目比较。
