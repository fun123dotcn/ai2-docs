# AI2 中文文档自动部署说明

## 部署架构

```
源仓库: fun123dotcn/ai2-docs (文档源码)
    ↓ GitHub Actions 自动构建
站点仓库: fun123dotcn/fun123dotcn.github.io (静态站点)
    ↓ GitHub Pages
访问地址: https://fun123dotcn.github.io/
```

## 使用方式

### 方式1：本地一键部署

```bash
cd ~/.qclaw/workspace/ai2-docs
./scripts/auto-deploy.sh "更新说明"
```

### 方式2：推送自动部署

```bash
# 修改文档后推送到源仓库
git add content/
git commit -m "新增文章: xxx"
git push origin main
# GitHub Actions 自动触发部署
```

### 方式3：手动触发部署

在 GitHub 仓库页面 → Actions → Deploy to GitHub Pages → Run workflow

## 首次配置

### 1. 创建 GitHub Token

1. 访问 https://github.com/settings/tokens/new
2. 选择 `fun123dotcn` 账号
3. 勾选权限：`repo` (全部)
4. 生成 Token 并复制

### 2. 添加 Secret

```bash
cd ~/.qclaw/workspace/ai2-docs
gh secret set FUN123_GH_TOKEN
# 粘贴 Token，按 Ctrl+D 结束
```

### 3. 验证

```bash
gh secret list
# 应显示: FUN123_GH_TOKEN
```

## 代理配置

脚本自动检测 `127.0.0.1:1087` 代理，如需修改：

```bash
# 编辑脚本
vim scripts/auto-deploy.sh
# 修改 PROXY_HOST 和 PROXY_PORT
```

## 仓库地址

- 源码：https://github.com/fun123dotcn/ai2-docs
- 站点：https://github.com/fun123dotcn/fun123dotcn.github.io
- 访问：https://fun123dotcn.github.io/

## 故障排查

### 编译失败

```bash
# 检查 Node 版本（需要 20.x）
node -v

# 重新安装依赖
rm -rf node_modules
npm install @mintlify/cli@4 --save-dev
```

### 推送失败

```bash
# 检查代理
curl --proxy http://127.0.0.1:1087 https://github.com

# 检查账号
gh auth status
```

### GitHub Actions 失败

1. 检查 Secret 是否设置：`gh secret list`
2. 检查 Token 权限：需要 `repo` 权限
3. 查看 Actions 日志定位错误
