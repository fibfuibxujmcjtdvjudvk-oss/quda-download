# 趣嗒APP下载页面

域名：**qovd.cn**

## 文件结构

```
download-page/
├── index.html      # 主下载页面
├── privacy.html    # 隐私政策
├── terms.html      # 用户协议
├── assets/         # 静态资源
│   ├── favicon.png # 网站图标（需添加）
│   └── qrcode.png  # 下载二维码（需添加）
└── download/       # APK下载目录
    └── quda.apk    # Android安装包（需添加）
```

## 部署步骤

### 方案一：Vercel（推荐，免费）

1. **注册 Vercel**
   - 访问 https://vercel.com
   - 使用 GitHub 账号登录

2. **上传代码**
   - 将 `download-page` 文件夹推送到 GitHub 仓库
   - 或直接在 Vercel 中拖拽上传

3. **绑定域名**
   - 在 Vercel 项目设置中添加域名 `qovd.cn`
   - 在域名DNS中添加记录：
     - 类型：CNAME
     - 主机记录：@（或 www）
     - 记录值：cname.vercel-dns.com

4. **等待生效**
   - DNS 生效需要 5-30 分钟
   - Vercel 自动配置 HTTPS

### 方案二：Netlify（免费）

1. 访问 https://netlify.com
2. 拖拽 `download-page` 文件夹上传
3. 在 Domain settings 中添加自定义域名
4. 按提示配置 DNS

### 方案三：阿里云OSS + CDN

1. 创建 OSS Bucket（设为公共读）
2. 上传所有文件
3. 开启静态网站托管
4. 配置 CDN 加速
5. 绑定域名并配置 HTTPS

## 需要准备的文件

1. **favicon.png** - 网站图标（建议 32x32 或 64x64）
2. **qrcode.png** - 下载页二维码（建议 200x200）
3. **quda.apk** - Android 安装包

## 生成二维码

可以使用以下工具生成下载页二维码：
- 草料二维码：https://cli.im
- 二维码生成器：https://www.qrcode-monkey.com

二维码内容填写：`https://qovd.cn`

## 注意事项

1. APK 文件较大，建议使用 CDN 加速
2. iOS 版本需要上架 App Store 后更新链接
3. 定期更新版本号和更新时间
4. 确保隐私政策和用户协议内容完整合规
