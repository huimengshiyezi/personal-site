# 上线说明

这个目录是**自动生成的**（源在 `../个人站/`），不要在这里改东西。

重新生成：`node _dev/prep-deploy.mjs --apply`

## 里面有什么

- `index.html` —— 主页
- `images/` —— 获奖证书 + 公众号二维码
- `tools/` —— 3 个工具（全部单文件、零依赖）

## 跟源目录的差别

**排除了 3 个不该公开的文件**：
- `images/README.md`（含本机路径）
- `tools/README.md`（内部构建说明）
- `tools/prompt-builder.template.html`（源文件，会暴露构建方式）

## 上线步骤（腾讯云 EdgeOne Pages）

1. 打开 https://edgeone.ai/zh/products/pages ，用微信或 QQ 登录
2. 新建项目 → 选「**直接上传**」（不用连 Git）
3. 把这个 `_deploy` 文件夹里的**全部内容**拖进去
   ⚠️ 拖的是**文件夹里面的东西**，不是文件夹本身 —— 让 `index.html` 在根目录
4. 等几十秒，会给你一个 `xxx.edgeone.app` 的免费域名
5. 打开那个域名验收

## 验收清单

- [ ] 主页能打开，4 张证书图都能显示
- [ ] 二维码图能显示（点「关注公众号」能看到）
- [ ] 点「AI 生图提示词装配台」能打开工具
- [ ] 工具里选几个词、点复制、点分享链接，都正常
- [ ] **手机上打开也正常**（重点看工具，拖动不卡、按钮够大）
- [ ] 换个网络（手机流量）再打开一次，确认不是只有本机能访问

## 以后更新

改完源文件 → `node _dev/build-prompt-builder.mjs`（如果改的是工具）→ `node _dev/prep-deploy.mjs --apply` → 重新上传。
