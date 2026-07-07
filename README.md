# zblog-l-plugin


#1、超级右键菜单
https://github.com/user-attachments/files/29669167/ZooVox_SuperMenu_3.0.5_2026-07-05.zip

14+
内置功能
首页、后退、前进、刷新、复制、全选、搜索、翻译等

5
预设主题
默认浅色、暗夜黑、深海蓝、清新绿、优雅紫

+
菜单分组
功能按类别分组展示，结构清晰，支持自定义链接

*
智能触发
支持自定义触发区域和排除区域，输入框自动保留默认菜单

kb
键盘导航
完善的键盘操作支持和无障碍访问

~
动画效果
流畅的显示和隐藏动画，提升用户体验
更新历史 （已添加到插件描述中）：

- v3.0.5 (2026-07-05) ：新增5款预设主题、可视化颜色选择器、圆角和阴影自定义
- v3.0.4 (2026-07-05) ：修复自定义链接显示为代码问题
- v3.0.3 (2026-07-05) ：修复菜单初始化时机问题
- v3.0.2 (2026-07-05) ：修复PHP 7+兼容问题
- v3.0.1 (2026-07-05) ：修复页面类型检测问题
- v3.0.0 (2026-07-05) ：完全重写插件，新增14+内置功能

鸣谢信息 ：
 参考版本：Jz52_rmenu v1.0.0
 鸣谢：感谢原作者提供的参考代码，本插件基于原插件理念进行了全面重写和功能扩展。


 
 #2、图床外链助手
 (https://github.com/zoovox1986/zblog-l-plugin/releases)
 

 功能简介
图床外链助手是一款功能强大的图片外链插件，自动将文章图片上传到图床服务器，减轻服务器带宽压力。

8+内置图床：包括最稳定的 GitHub + jsDelivr、国内速度快的路过图床等
自定义图床：支持添加任意图床API，灵活配置上传参数和响应解析
自动替换：上传图片自动替换为图床链接，支持全局/文章模式切换
粘贴同步：编辑器中粘贴图片时自动上传到图床
统计管理：支持查看各图床上传数量，方便管理
安全回退：停用图床自动回退到本地图片，不影响网站正常显示

内置图床
图床名称	特点	推荐理由
GitHub + jsDelivr CDN 最推荐	完全免费、无限流量、全球CDN加速、永久存储	数据由GitHub保障，稳定性最高，适合长期使用
路过图床 imgtu.com	国内运营、速度快、支持API上传、单图最大10MB	国内访问速度快，运营时间长，稳定性好
蜜蜂图床 beeimg.cn	国内节点、加载快、RESTful API、加密存储	纯国内节点，上传下载速度快，API文档完善
图壳 imgkr.com	国内CDN、无压缩、直链稳定、界面极简	图片不压缩，国内CDN加速，界面简洁
Postimages	国外稳定、API支持、免费额度充足	运营时间长，API稳定，免费额度充足
Imgur	全球最大图床、支持匿名上传、无需注册	全球最大图床，CDN遍布全球，无需注册
ImgTP	免登录、不压缩画质、支持PicGo集成	不压缩画质，保留原图质量
自定义图床	支持添加任意图床API	灵活配置，满足特殊需求
使用说明
1. 安装插件
在 Z-BlogPHP 后台 → 应用中心 → 上传插件，选择下载的 zoovox_imagehosting_2.5.1_2026-07-06.zba 文件进行安装。

2. 选择图床
进入插件配置页面，点击选择一个图床。建议优先选择 GitHub + jsDelivr CDN（最稳定）或国内图床（速度快）。

3. 配置认证信息
选择图床后会自动展开对应的配置面板：

路过图床：需配置 API Token（登录 imgtu.com 后在个人中心获取）
GitHub + jsDelivr：需配置 Personal Access Token 和仓库信息
其他图床：无需额外配置，直接使用
4. 全局模式
开启后会替换前台所有页面的图片链接，关闭则只替换文章内容中的图片。

5. 文章编辑
编辑文章时，如果有未上传到图床的图片，会显示"将文章内的图片上传到图床"选项，开启后提交文章会自动上传。

6. 粘贴图片
在编辑器中粘贴图片时，插件会自动检测并将图片上传到图床，无需手动操作。

GitHub + jsDelivr CDN 配置步骤
创建一个公开的 GitHub 仓库（必须是 Public）
生成 Personal Access Token：Settings → Developer settings → Personal access tokens → Generate new token
勾选 repo 权限，复制生成的 Token（只显示一次，务必保存）
填写仓库地址（格式：username/repository）
选择"GitHub + jsDelivr CDN"作为当前图床即可使用
生成的图片链接格式：https://cdn.jsdelivr.net/gh/username/repository@main/images/20260705_xxx.png
本地文件与稳定性说明
本地文件保留：启用图床后，图片会同时保存在您的服务器和图床服务器。插件不会删除任何本地文件。
智能回退机制：当某个图床服务不可用时，只需勾选"停用"该图床，文章会自动使用本地图片链接，不影响网站正常显示。
免费图床风险：免费图床服务可能会因运营调整、政策变化等原因停止服务或删除图片。重要图片建议保留本地备份。
双重保险：本地文件作为原始备份，图床链接用于展示。即使图床失效，本地文件依然可用，随时可以回退。



更新历史

v4.1.3 (2026-07-07)

修复 已上传图片跳过逻辑：统一 get_upload_list.php、batch_upload.php、include.php 的跳过判断规则
修复 旧版本兼容：支持 tuchuang_api 为空但 tuchuang 已设置的旧记录正确跳过，避免重复上传
修复 文章编辑上传：仅当 tuchuang 为空时才上传，不再因 tuchuang_api 不匹配而重复上传

v4.1.2 (2026-07-07)

修复 路过图床：添加完整日志记录，支持匿名上传回退，修复配置参数无法保存问题
修复 ImgBB：移除默认过期API Key，强制用户配置有效Key，API调用方式符合官方规范
修复 sm.ms：API端点从 sm.ms/api/v2/upload 迁移到 s.ee/api/v1/file/upload，添加Token认证配置
修复 postimages.org：API端点从 /upload 改为 /json，添加X-Requested-With头
修复 catbox.moe：强制HTTP/1.1连接，修复HTTP/2流错误
新增 sm.ms配置面板：支持填写API Token，可选匿名上传
修复 POST白名单：添加 imgchr_username、imgchr_password、imgur_client_id、imgbb_api_key、smms_token
修复 配置面板切换：添加sm.ms配置面板的实时切换


v4.1.0 (2026-07-06)

修复 插件启用失败：打包结构错误，压缩包内缺少根目录 zoovox_imagehosting/
新增 ImgPile（imgpile.com）：国外免费图床，单图最大200MB，直链稳定
新增 时光图床（shiguangtc.com）：国内免费图床，无需注册，支持直链
新增 ImgBB（imgbb.com）：国外免费图床，单图最大32MB，直链稳定
图床分类调整：重新组织为「最推荐」「国内图床」「国外图床」「自定义图床」
GitHub + jsDelivr：添加国内DNS污染风险提示


【重大更新】v4.0.0 (2026-07-06)

新增 Cloudflare R2 图床：每月10GB免费空间，读写流量完全免费，全球CDN加速，抗封禁能力强
新增 聚合图床（superbed.cn）：国内商业运营，免费基础版更持久
更新 路过图床：API端点从 imgtu.com 迁移到 imgse.com
移除 蜜蜂图床（beeimg.cn）：服务不稳定，HTTP 500错误频繁
移除 图壳（imgkr.com）：域名已失效
移除 ImgTP（imgtp.com）：域名已出售
修复 sm.ms：移除空 Authorization 头，支持匿名上传
修复 postimages.org：更新API端点为 api.postimages.org/json
新增 重置上传状态功能：仅清除当前图床的上传记录，可重新上传
新增 切换图床后可重新上传已在其他图床上传过的图片
统计功能：修复"查看各图床上传数量"显示为空的问题
统计功能：修复"一键处理"统计包含已上传图片的问题


v3.4.0 (2026-07-06)

GitHub图床：新增CDN线路选择功能，支持多条优质稳定备用线路
CDN选项：jsDelivr默认、Fastly CDN、Cloudflare CDN、Gcore CDN、自定义CDN
自定义CDN：支持手动输入自定义CDN地址，应对jsDelivr失效或被污染的情况
一键处理：修复fetchUploadList错误处理，添加超时和网络错误提示


v3.3.0 (2026-07-06)

GitHub API：新增 Accept: application/vnd.github.v3+json 请求头，符合官方API规范
批量上传：间隔从500ms增加到2000ms，符合GitHub限流要求
限流处理：新增403/429错误检测，触发时自动停止并弹窗提示
文件验证：新增单图≤10MB大小限制，拒绝超大原图上传
Token安全：确保Token仅存储在后台配置，不输出到前端页面


v3.2.0 (2026-07-06)

GitHub图床：增加完整防封禁教程，包含5个步骤配置指南
GitHub图床：推荐按用途分类存储路径（blog/、notes/、tutorial/），避免堆在根目录
GitHub图床：提供仓库README英文合规模板，完善仓库信息降低封禁风险
GitHub图床：新增日常使用规范（图片压缩、仓库容量监控、季度Token轮换等）

v3.1.0 (2026-07-06)

蜜蜂图床：新增 API Key 配置（可选），游客模式每分钟限传1张，填写API Key提升配额
GitHub图床：添加使用警示，建议使用细粒度 Fine-grained Token，单次上传≤10张，间隔30秒以上
蜜蜂图床API更新：使用官方最新接口 beeimg.com/api/upload/file/json/
修复：新增蜜蜂图床配置面板动态显示逻辑
【重大更新】v3.0.0 (2026-07-06)

新增一键处理所有文章图片功能：批量上传历史图片到图床
采用AJAX逐张上传方案，避免PHP超时和图床限流
仅更新图片元数据，绝不修改文章内容，确保安全
已上传图片自动跳过，支持中断续传
实时进度追踪，显示成功/失败/跳过数量
新增 batch_upload.php 和 get_upload_list.php 接口文件

v2.5.1 (2026-07-06)
紧急修复：include.php 文件被截断导致 "syntax error, unexpected end of file" 致命错误
补全 zoovox_imagehosting_getuploadbyurl 函数缺失的代码

v2.5.0 (2026-07-05)
修复统计数量查询错误，修复 database escape 方法不存在问题
修复输出缓冲安全问题，添加安全检查和异常处理
所有钩子注册已移至 ActivePlugin 函数内部，避免插件停用后仍执行

v2.4.0 (2026-07-05)
修复卡片点击选中功能，确保点击卡片任意位置都能选中
恢复卡片悬停变色效果
优化操作按钮布局，修复保存配置按钮显示不全问题
实现编辑器粘贴图片自动同步到图床功能

v2.3.0 (2026-07-05)
增加图床选项选中区域，整个卡片均可点击选择
优化保存配置和查看数量按钮位置，使用操作栏布局
修复统计数量一直为0的问题，改用正确的数据库查询方式
调整停用复选框位置，避免点击冲突

v2.2.0 (2026-07-05)
重构配置页面布局，采用卡片式设计
图床配置面板改为内联展开式，选中后自动显示
修复自定义图床单选按钮位置问题
合并信息区块，精简页面内容
添加平滑展开动画效果

v2.1.0 (2026-07-05)
新增 GitHub + jsDelivr CDN 图床
新增路过图床（imgtu.com）
图床分类展示，顶部标注最推荐图床
默认图床改为 GitHub + jsDelivr CDN

v2.0.0 (2026-07-05)
完全重写插件，更新应用ID为 zoovox_imagehosting
新增蜜蜂图床、图壳、Postimages、Imgur、ImgTP
新增自定义图床功能
移除已失效的旧图床接口

