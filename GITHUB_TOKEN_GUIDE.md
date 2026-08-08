# 🔑 How to Generate GitHub Personal Access Token (PAT)

## Why You Need a Token

GitHub no longer accepts passwords for Git operations. You need a **Personal Access Token (PAT)** for authentication.

---

## Step 1: Go to GitHub Settings

1. Open: https://github.com
2. Log in to your account
3. Click your **profile icon** (top right)
4. Click **Settings**

---

## Step 2: Navigate to Personal Access Tokens

1. In the left sidebar, scroll down
2. Click **Developer settings**
3. Click **Personal access tokens**
4. Click **Tokens (classic)**

---

## Step 3: Generate New Token

1. Click **Generate new token** button
2. Select **Generate new token (classic)**

---

## Step 4: Configure Token Settings

Fill in the following:

### Token Name
```
Conversational_AI_Push
```

### Expiration
Choose one of:
- **7 days** (most secure, but need new token often)
- **30 days** (balanced)
- **90 days** (default, recommended)
- **No expiration** (convenient but less secure)

### Select Scopes
Check the following box:
```
✅ repo (Full control of private repositories)
```

This will automatically check:
- ✅ repo:status
- ✅ repo_deployment
- ✅ public_repo
- ✅ repo:invite
- ✅ security_events

---

## Step 5: Generate Token

Click the **Generate token** button at the bottom.

---

## Step 6: Copy Your Token

⚠️ **IMPORTANT:** You'll see your token only ONCE!

```
ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

**COPY this token immediately** and save it somewhere safe:
- ✅ Save in a text editor temporarily
- ✅ Save in a password manager
- ⚠️ Do NOT share it
- ⚠️ Do NOT commit it to Git

---

## Step 7: Use Token to Push Code

Once you have your token, push your code:

```bash
cd /Users/surajuniyal/Desktop/Conversational_AI

git push -u origin main
```

When Git asks for credentials:

```
Username for 'https://github.com': surajuniyal073
Password for 'https://surajuniyal073@github.com': [PASTE YOUR TOKEN HERE]
```

**Copy and paste your token as the password** (right-click or Cmd+V)

---

## Complete Visual Guide

```
GitHub.com
    ↓
Login
    ↓
Profile Icon (top right)
    ↓
Settings
    ↓
Developer Settings (left sidebar)
    ↓
Personal Access Tokens
    ↓
Tokens (classic)
    ↓
Generate new token (classic)
    ↓
Fill in name & scopes
    ↓
Generate token
    ↓
COPY token (you won't see it again!)
    ↓
Use for git push
```

---

## Quick Reference URLs

| What | URL |
|------|-----|
| Create Token | https://github.com/settings/tokens |
| GitHub Settings | https://github.com/settings |
| Developer Settings | https://github.com/settings/developers |
| New Repository | https://github.com/new |

---

## Token Format

Your token will look like:

```
ghp_1234567890abcdefghijklmnopqrstuvwxyz
```

- Starts with: `ghp_`
- Length: ~40 characters
- Hexadecimal: Contains 0-9, a-f

---

## How to Use Token with Git

### Option 1: Use Token When Prompted (Easiest)

```bash
git push -u origin main

# When prompted:
# Username: surajuniyal073
# Password: ghp_xxxx... (paste your token)
```

### Option 2: Include in URL

```bash
git push -u origin https://surajuniyal073:ghp_xxxx...@github.com/surajuniyal073/assignment2_Converstational_AI.git main
```

⚠️ Not recommended - token visible in command history

### Option 3: Use Git Credentials Manager (Recommended)

```bash
# Set up credentials caching
git config --global credential.helper osxkeychain

# First push asks for token, then it's remembered
git push -u origin main
```

---

## Token Permissions Explained

When you select **repo**, you get:

| Permission | What it allows |
|-----------|----------------|
| `repo:status` | Access repository status |
| `repo_deployment` | Deploy to production |
| `public_repo` | Read/write public repos |
| `repo:invite` | Accept repo invitations |
| `security_events` | Read/write security events |

For simple push, only `public_repo` or `repo` is needed.

---

## Security Best Practices

✅ **DO:**
- Create token with minimal needed permissions
- Set expiration date
- Use different tokens for different purposes
- Store safely (password manager)
- Regenerate periodically

❌ **DON'T:**
- Share your token
- Commit token to Git
- Use no-expiration tokens
- Give more permissions than needed
- Leave token visible on screen

---

## If You Lose Your Token

If you forget to copy your token:

1. Go back to: https://github.com/settings/tokens
2. Your token is no longer visible
3. Delete that token
4. Generate a new one
5. Follow steps above again

---

## If Your Token Expires

When your token expires:

1. Go to: https://github.com/settings/tokens
2. Find your expired token (will show "Expired")
3. Regenerate it or create a new one
4. Git will ask for new credentials on next push

---

## Complete Push Workflow

```bash
# 1. Make sure you're in the right directory
cd /Users/surajuniyal/Desktop/Conversational_AI

# 2. Configure credentials manager (one time)
git config --global credential.helper osxkeychain

# 3. Push your code
git push -u origin main

# 4. When prompted, enter:
#    Username: surajuniyal073
#    Password: [paste your token]

# 5. Done! Your code is on GitHub 🎉
```

---

## Verify Push Worked

After pushing, check:

```bash
# Check if push succeeded
git remote -v

# View push confirmation
git log --oneline

# Go to GitHub in browser:
# https://github.com/surajuniyal073/assignment2_Converstational_AI
```

You should see all your files and commits on GitHub.

---

## Troubleshooting Token Issues

### Error: "Authentication failed"
**Cause:** Wrong token or expired
**Solution:** 
1. Generate new token
2. Use new token for push

### Error: "Invalid username or token"
**Cause:** Token copied incorrectly
**Solution:**
1. Get token again (make sure you copy ALL of it)
2. Check username is correct: `surajuniyal073`
3. Try again

### Error: "Password authentication not supported"
**Cause:** Trying to use password instead of token
**Solution:**
1. Generate Personal Access Token (this guide)
2. Use token as password

### Error: "Could not read Username"
**Cause:** No credentials manager configured
**Solution:**
1. Run: `git config --global credential.helper osxkeychain`
2. Try push again

---

## How Long Token Lasts

Typical token lifespans:

| Duration | When to use |
|----------|------------|
| 7 days | Very sensitive work, maximum security |
| 30 days | Regular work, good balance |
| 90 days | Default, normal usage |
| No expiration | Personal projects, trusted machines |

---

## After Successful Push

Your GitHub repo will have:

✅ All your files
✅ All your commits
✅ Full history
✅ Publicly accessible (or private)

Then you can:
- Share the link
- Add to your portfolio
- Collaborate with others
- Keep as backup

---

## FAQ

**Q: How many tokens can I have?**
A: Unlimited. Create separate tokens for different projects.

**Q: Can I use same token everywhere?**
A: Yes, but not recommended. Different tokens for different uses is safer.

**Q: What if I share my token accidentally?**
A: Go to GitHub tokens page and delete it immediately. Create new one.

**Q: Can I regenerate same token?**
A: No. You have to delete and create new one.

**Q: How do I know if token is valid?**
A: Try using it for a push. If it works, it's valid.

**Q: Can I see my token after creating it?**
A: No, only on creation. If you lose it, delete and create new one.

---

## Next Steps

1. ✅ Create your Personal Access Token
2. ✅ Copy and save it safely
3. ✅ Run: `git config --global credential.helper osxkeychain`
4. ✅ Run: `git push -u origin main`
5. ✅ Enter token when prompted
6. ✅ Verify on GitHub
7. ✅ Done! 🚀

---

## Your Repository After Push

```
https://github.com/surajuniyal073/assignment2_Converstational_AI

Files:
✅ Multi_Agent_RAG_System.ipynb (86 KB)
✅ All documentation files
✅ Original assignment
✅ .gitignore

Commits:
✅ 5 commits with messages
✅ Full history visible
✅ All changes tracked

Ready for:
✅ Sharing
✅ Portfolio
✅ Collaboration
```

---

## Support

If you get stuck:
- Check GitHub docs: https://docs.github.com
- See DO_THIS_NOW.md for simpler guide
- See AUTHENTICATION_NEEDED.md for more help

---

**You've got this! 🎉 Create your token and push your code!**
