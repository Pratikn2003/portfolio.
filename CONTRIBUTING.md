# What to Do When Code Changes

This guide explains the workflow for making changes to this portfolio website.

## Quick Overview

When you make changes to your code:
1. **Edit** your files locally
2. **Commit** your changes using Git
3. **Push** to GitHub
4. **Automatic Deployment** - GitHub Actions will deploy your changes to GitHub Pages

---

## Step-by-Step Guide

### 1. Make Your Changes

Edit the files you want to change. For this portfolio, you'll typically edit:
- `index.html` - The main portfolio page (HTML, CSS, and JavaScript)
- Image files - Add or replace photos

### 2. Check What Changed

Open your terminal and run:
```bash
git status
```
This shows which files you've modified, added, or deleted.

To see the exact changes in a file:
```bash
git diff index.html
```

### 3. Stage Your Changes

Add the files you want to include in your commit:
```bash
# Add specific files
git add index.html

# Or add all changed files
git add .
```

### 4. Commit Your Changes

Create a commit with a descriptive message:
```bash
git commit -m "Your description of what changed"
```

**Good commit message examples:**
- `"Update contact information"`
- `"Add new project to portfolio section"`
- `"Fix navigation menu on mobile"`
- `"Update profile photo"`

### 5. Push to GitHub

Send your changes to GitHub:
```bash
git push origin main
```

### 6. Automatic Deployment

Once you push to the `main` branch:
- GitHub Actions automatically runs
- Your website is deployed to GitHub Pages
- Changes are live within a few minutes!

You can check the deployment status:
1. Go to your repository on GitHub
2. Click on **Actions** tab
3. See the workflow run status

---

## Common Scenarios

### Scenario 1: Edit Your Portfolio Content

1. Open `index.html` in your code editor
2. Make your changes (update text, add sections, etc.)
3. Save the file
4. Run these commands:
   ```bash
   git add index.html
   git commit -m "Update portfolio content"
   git push origin main
   ```

### Scenario 2: Add a New Photo

1. Add the new image file to the repository folder
2. Update `index.html` to reference the new image
3. Run these commands:
   ```bash
   git add .
   git commit -m "Add new photo"
   git push origin main
   ```

### Scenario 3: Undo Recent Changes

If you made a mistake and want to undo changes that haven't been committed:
```bash
# Undo changes to a specific file
git restore index.html

# Undo all uncommitted changes
git restore .
```

---

## Tips and Best Practices

1. **Preview Locally First**: Open `index.html` in your browser to check changes before committing

2. **Make Small, Focused Commits**: Each commit should represent one logical change

3. **Write Clear Commit Messages**: Describe what changed and why

4. **Check Status Often**: Use `git status` to see where you are

5. **Pull Before Push**: If others work on the repo, run `git pull` before pushing

---

## Need Help?

- **Git Basics**: [Git Documentation](https://git-scm.com/doc)
- **GitHub Pages**: [GitHub Pages Documentation](https://docs.github.com/en/pages)
- **GitHub Actions**: Check the `.github/workflows/deploy.yml` file to see how automatic deployment works
