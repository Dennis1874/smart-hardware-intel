# GitHub 仓库设置指南

## 📋 步骤 1：在 GitHub 上创建新仓库

1. 访问 [GitHub.com](https://github.com) 并登录
2. 点击右上角的 **"+"** 按钮，选择 **"New repository"**
3. 填写以下信息：
   - **Repository name**: `smart-hardware-intel`
   - **Description**: `智能硬件情报中心 - Smart Hardware Intelligence Hub`
   - **Visibility**: 选择 **"Private"** (私有仓库，仅你可见)
   - **不要勾选** "Initialize this repository with a README"（因为我们已经有本地代码了）
4. 点击 **"Create repository"**

---

## 🔗 步骤 2：关联远程仓库并推送

创建仓库后，GitHub 会显示推送指令。在终端中执行以下命令：

```bash
cd /Users/dennis/.qoderwork/workspace/mmyis4jtoz7qmhty/smart-hardware-intel

# 添加远程仓库（将 <your-username> 替换为你的 GitHub 用户名）
git remote add origin https://github.com/<your-username>/smart-hardware-intel.git

# 验证远程仓库
git remote -v

# 推送到 GitHub
git branch -M main
git push -u origin main
```

---

## 🔐 身份验证方式

### 方式 A：使用 Personal Access Token（推荐）

1. 访问 [GitHub Settings > Developer settings > Personal access tokens](https://github.com/settings/tokens)
2. 点击 **"Generate new token (classic)"**
3. 填写说明（如 "QoderWork Git Access"）
4. 勾选权限：**`repo`** (Full control of private repositories)
5. 生成后复制 token（只显示一次！）
6. 推送时会提示输入密码，粘贴 token 即可

### 方式 B：使用 SSH Key

```bash
# 生成 SSH key（如果还没有）
ssh-keygen -t ed25519 -C "your-email@example.com"

# 查看公钥
cat ~/.ssh/id_ed25519.pub

# 将输出内容复制到 GitHub:
# Settings > SSH and GPG keys > New SSH key
```

---

## ✅ 验证推送成功

推送完成后，刷新 GitHub 仓库页面，你应该能看到所有文件：
- START-HERE.md
- README.md
- 01-news/README.md
- 02-technical-deep-dives/README.md
- 03-product-analysis/README.md
- 04-opportunities/README.md
- 05-investment/README.md
- 06-research/README.md
- focus-areas/*.md
- company-tracking/README.md

---

## 🔄 后续更新

每次自动搜集任务执行后，我会帮你提交更改并推送到 GitHub：

```bash
git add -A
git commit -m "Auto-update: YYYY-MM-DD - 本周期的信息更新"
git push
```

你也可以随时手动拉取最新内容：
```bash
git pull origin main
```

---

## 📱 移动端访问

设置完成后，你可以在任何设备上通过 GitHub 访问这些文档：
- GitHub App（iOS/Android）
- 移动网页版：`https://github.com/your-username/smart-hardware-intel`

---

## 🎯 下一步

完成推送后，告诉我，我会：
1. 验证仓库连接状态
2. 设置自动推送流程
3. 配置定期同步机制

---

**需要帮助吗？** 如果在设置过程中遇到任何问题，随时告诉我！
