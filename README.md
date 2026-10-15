# 九格突围官网

本地静态站，面向 `https://jiumen.funvalvar.com`，开发者 Funvalvar，支持邮箱 funvalvar@proton.me。没有框架、构建依赖、外部字体、统计或广告脚本。

## 本地预览

官网现位于 `/Users/zhangcheng/developer/my-projects/jiumen/sites/official-site`。

可以直接双击根目录或三语子目录中的 `index.html`，图片、样式、页面导航与语言切换均使用相对路径，无需启动服务。

需要浏览器HTTP预览时，在本目录运行 `python3 -m http.server 8765 --bind 127.0.0.1`，访问 `http://127.0.0.1:8765/`。若从父目录 `sites` 启动服务，则访问 `http://127.0.0.1:8765/official-site/`。

各页面内部链接显式指向对应的 `index.html`，兼容本地文件和HTTP子目录；正式部署仍可使用下列简洁目录地址。

## 页面与 Apple 字段

- 英文：首页 `/`，支持 `/support/`，隐私 `/privacy/`。
- 简中：首页 `/zh-Hans/`，支持 `/zh-Hans/support/`，隐私 `/zh-Hans/privacy/`。
- 繁中：首页 `/zh-Hant/`，支持 `/zh-Hant/support/`，隐私 `/zh-Hant/privacy/`。
- 语言切换保留所在页面类别。主要内容无需 JavaScript。
- 首页已标注展示画面来自 Web 版。图像不得转作 App Store iOS 截图。

## 部署

将本目录作为静态站根目录，配置 HTTPS 和上述域名，保留目录内的 `index.html` 路由。没有 SPA 回退需求；不存在的页面应返回404，不要重写至首页。确保图片、CSS、JS按正确 MIME 类型提供。

上传公开文件：9个页面及其目录、`assets/`、`robots.txt`、`sitemap.xml`。README、`app-ads.txt.example`及任何验收文件不用公开。不要上传 `apple-review/`，其中可能包含审核私人联系方式。

配置 DNS、证书、托管日志及保留期限后，核对隐私政策“本网站”和“保留期限”条款与实际托管行为一致。上线后逐一检查三语页面，无需登录即可访问，再填入 App Store Connect。

获得真实 App Store URL后，将各首页的“即将上线”状态改为真实下载链接。本次没有部署。

## AdMob app-ads.txt

在 AdMob → 应用 → app-ads.txt 设置复制完整授权销售商记录。使用后台提供的发布商ID、关系字段和认证机构ID；不得根据应用ID猜完整记录。创建根目录 `/app-ads.txt`，纯文本提供（HTTP 200），再在商店营销网址及 AdMob后台核对域名和抓取状态。当前仅提供示例说明文件，没有发布占位的 app-ads.txt。

## 更新原则

三语商店文案和官网共同基于 `0.2.0 (3)`。关卡、广告、数据处理方式或支持渠道变化时，同时更新对应页面和审核包。隐私政策日期应使用实际修订日期。
