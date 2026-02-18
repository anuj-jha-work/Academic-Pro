# 📤 Step-by-Step Upload Guide

This guide will help you upload your project from your laptop to this GitHub repository.

## Before You Start

### What You Need:
- Git installed on your computer ([Download Git](https://git-scm.com/downloads))
- A GitHub account
- Your project files ready on your laptop

### Quick Check:
- [ ] Git is installed (run `git --version` in terminal)
- [ ] You have access to this repository
- [ ] Your project is in a single folder

## Method 1: Command Line (Recommended)

### Step 1: Open Terminal/Command Prompt

- **Windows**: Press `Win + R`, type `cmd`, press Enter
- **Mac**: Press `Cmd + Space`, type `terminal`, press Enter
- **Linux**: Press `Ctrl + Alt + T`

### Step 2: Navigate to Your Project Folder

```bash
# Example: If your project is in Documents/MyProject
cd Documents/MyProject

# Or use the full path
cd C:\Users\YourName\Documents\MyProject  # Windows
cd /Users/YourName/Documents/MyProject    # Mac/Linux
```

### Step 3: Initialize Git (if not done already)

```bash
git init
```

You should see: `Initialized empty Git repository...`

### Step 4: Add All Files

```bash
git add .
```

This stages all your files for commit.

### Step 5: Make Your First Commit

```bash
git commit -m "Initial commit - Upload my academic project"
```

### Step 6: Connect to GitHub

```bash
git remote add origin https://github.com/anuj-jha-work/Academic-Pro.git
```

### Step 7: Pull Existing Files (to merge with README)

```bash
git pull origin main --allow-unrelated-histories
```

If you see a merge editor, just save and exit (`:wq` in Vim, or `Ctrl+X` in nano).

### Step 8: Push Your Project

```bash
git branch -M main
git push -u origin main
```

### Step 9: Enter Credentials

- **Username**: Your GitHub username
- **Password**: Use a Personal Access Token (NOT your GitHub password)
  - Generate one here: https://github.com/settings/tokens
  - Select `repo` scope
  - Copy the token and paste it as password

## Method 2: GitHub Desktop (Easier for Beginners)

### Step 1: Install GitHub Desktop

Download from: https://desktop.github.com/

### Step 2: Sign In

- Open GitHub Desktop
- Click "File" → "Options" → "Accounts"
- Sign in with your GitHub account

### Step 3: Clone the Repository

- Click "File" → "Clone repository"
- Select the "GitHub.com" tab
- Find `anuj-jha-work/Academic-Pro`
- Choose where to save it on your computer
- Click "Clone"

### Step 4: Add Your Files

- Open the folder where you cloned the repository
- Copy ALL your project files into this folder
- You can drag and drop or use copy-paste

### Step 5: Commit Changes

- Go back to GitHub Desktop
- You'll see all your new files listed
- In the bottom left:
  - Summary: "Upload my academic project"
  - Description: (optional) Add more details
- Click "Commit to main"

### Step 6: Push to GitHub

- Click "Push origin" button at the top
- Wait for the upload to complete

## Method 3: Web Interface (For Small Projects Only)

⚠️ **Limitations**: Max 25MB per file, 100 files at once

### Step 1: Go to Repository

Visit: https://github.com/anuj-jha-work/Academic-Pro

### Step 2: Upload Files

- Click "Add file" → "Upload files"
- Drag and drop your files
- Or click "choose your files" to browse

### Step 3: Commit

- Scroll down
- Add commit message: "Upload my academic project"
- Click "Commit changes"

## Troubleshooting

### Problem: "Permission denied"

**Solution**: Generate a Personal Access Token
1. Go to: https://github.com/settings/tokens
2. Click "Generate new token (classic)"
3. Give it a name: "Academic-Pro Upload"
4. Select scope: `repo`
5. Click "Generate token"
6. Copy the token and use it as your password

### Problem: "Large files" error

**Solution**: Use Git LFS for files over 100MB
```bash
git lfs install
git lfs track "*.zip"
git lfs track "*.psd"
git add .gitattributes
git commit -m "Add Git LFS"
git push
```

### Problem: "Repository not found"

**Solution**: Check the repository URL and your permissions
```bash
git remote -v  # Check current remote
git remote set-url origin https://github.com/anuj-jha-work/Academic-Pro.git
```

### Problem: "Merge conflicts"

**Solution**: Accept both changes
```bash
git pull origin main --allow-unrelated-histories
# If conflicts occur:
git add .
git commit -m "Merge existing files"
git push
```

## Verify Upload

After uploading, verify by:

1. **Go to**: https://github.com/anuj-jha-work/Academic-Pro
2. **Check**: All your files should be visible
3. **Test**: Clone the repository to a different location and try running it

```bash
cd /tmp
git clone https://github.com/anuj-jha-work/Academic-Pro.git
cd Academic-Pro
# Try running your project
```

## Next Steps

After successful upload:

- [ ] Update the README.md with your project details
- [ ] Add a LICENSE file (if needed)
- [ ] Create a .gitignore for unwanted files
- [ ] Test that others can clone and run your project

## Need More Help?

- **GitHub Docs**: https://docs.github.com/
- **Git Basics**: https://git-scm.com/book/en/v2
- **Video Tutorial**: Search "How to push code to GitHub" on YouTube

---

**Still stuck?** Create an issue in this repository or contact your instructor!
