Claude 表情包使用说明

图片仓库：https://github.com/ririclaude/claude-stickers
最新目录：https://raw.githubusercontent.com/ririclaude/claude-stickers/main/catalog.json
图片基础地址：https://cdn.jsdelivr.net/gh/ririclaude/claude-stickers@main/

将本说明和 catalog.json 加入 Claude 项目文件。聊天时根据 meaning 自然选一张，使用该条的完整 url；没有标注含义的先看图，不凭编号猜。保留真实扩展名。

先调用当前可用的 visualize:read_me 阅读要求，再用 visualize:show_widget 显示 img。实际调用参数以当前工具说明为准。图片建议 width:160px;border-radius:12px;display:block。不要只输出 HTML 文本，也不要把输出标记当成发送成功。

先测试：https://cdn.jsdelivr.net/gh/ririclaude/claude-stickers@main/86ab46c3.jpeg
这张的含义是“贴贴 贴贴”。先确认聊天界面中实际显示了图片，再用于日常聊天。若加载失败，如实说明。

新增图片时：保持旧文件名不变，给新图分配独立 ID，保留原始格式，并更新 catalog.json。用户说“图库更新了”时，重新读取最新目录；若当前环境无法读取，请用户上传新版 catalog.json，不要声称已经同步。上传到 Claude 项目的旧目录不会自行更新。

尺寸：catalog.json 中 width/height 是原图像素；display_width/display_height 是显示宽度160px时的预留尺寸，显示高度四舍五入。图片用 object-fit:contain 保持比例，外框按同样显示尺寸预留，不加多余 min-height 或上下留白。若客户端仍有空白，需要区分宿主组件默认间距，不继续盲目改图片比例。
若 Claude 当前无法联网读取目录，直接粘贴目录与尺寸；不要仅靠“图库更新了”这句话。
