# 📸 Visual Guide: Step-by-Step Token Generation

## Screen 1: GitHub Home
```
Go to: https://github.com
Log in with your credentials
    ↓
You should see your dashboard
```

---

## Screen 2: Profile Settings
```
Click your profile icon (top right corner)
    ↓
A dropdown menu appears
    ↓
Click "Settings"
```

Screenshot area:
```
╔═══════════════════════════════════════╗
║ GitHub                                ║
║  [🔍] [🔔] [⚙️ Settings] [👤 Profile]║  ← Your icon top right
╚═══════════════════════════════════════╝
      ↓
   Click ⚙️ Settings
```

---

## Screen 3: Settings Sidebar
```
Left sidebar with many options:
   • Profile
   • Account
   • ...
   (scroll down)
   ↓
   • Developer settings ← Click here
```

Location: Bottom left of settings page

---

## Screen 4: Developer Settings
```
Left sidebar now shows:
   • Personal access tokens
   • OAuth apps
   • GitHub Apps
   
Click: "Personal access tokens"
   ↓
Click: "Tokens (classic)"
```

---

## Screen 5: Tokens Page
```
You see a list of your tokens (probably empty first time)

Button at top right:
┌─────────────────────────────┐
│ Generate new token ▼        │
└─────────────────────────────┘
   ↓
Click the dropdown arrow ▼
   ↓
Click "Generate new token (classic)"
```

---

## Screen 6: Create New Token Form
```
┌─────────────────────────────────────────────┐
│ Create a new personal access token (classic)│
├─────────────────────────────────────────────┤
│                                             │
│ Token name *                                │
│ ┌─────────────────────────────────────────┐ │
│ │ Conversational_AI_Push                  │ │ ← Enter this
│ └─────────────────────────────────────────┘ │
│                                             │
│ Expiration                                  │
│ ┌─────────────────────────────────────────┐ │
│ │ 90 days ▼                               │ │ ← Select 90 days
│ └─────────────────────────────────────────┘ │
│                                             │
│ Select scopes                               │
│ ┌─────────────────────────────────────────┐ │
│ │ ☑ repo                                  │ │ ← Check this
│ │   (Full control of private repos)       │ │
│ │ ☐ workflow                              │ │
│ │ ☐ write:packages                        │ │
│ │ ...more options...                      │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ Generate token                          │ │ ← Click here
│ └─────────────────────────────────────────┘ │
│                                             │
└─────────────────────────────────────────────┘
```

---

## Screen 7: Token Generated! ⚠️ IMPORTANT

```
┌─────────────────────────────────────────────────────────┐
│ ⚠️ Make sure to copy your new personal access token now │
│ You won't be able to see it again!                      │
├─────────────────────────────────────────────────────────┤
│                                                         │
│ ghp_1234567890abcdefghijklmnopqrstuvwxyz123456789      │
│                                                         │
│ [📋 Copy to clipboard]  [👁️ Show/Hide]                 │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**ACTION: Click "Copy to clipboard" button or select and copy**

The token looks like:
```
ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

---

## Screen 8: Save Your Token

Save it in a safe place:

**Option A: Text Editor**
```
Paste in a text file temporarily:
surajuniyal073_token.txt (keep this private!)
ghp_1234567890abcdefghijklmnopqrstuvwxyz
```

**Option B: Password Manager**
```
1Password / LastPass / Bitwarden
Service: GitHub
Username: surajuniyal073
Token: ghp_xxxx...
```

**Option C: Keychain (Mac)**
```
Will be stored automatically when you use it
(thanks to: git config --global credential.helper osxkeychain)
```

---

## Screen 9: Use Token for Git Push

Open Terminal:

```bash
cd /Users/surajuniyal/Desktop/Conversational_AI

git config --global credential.helper osxkeychain

git push -u origin main
```

---

## Screen 10: Git Asks for Credentials

Terminal shows:
```
Username for 'https://github.com': _
```

Type your username:
```
Username for 'https://github.com': surajuniyal073
```

Then press Enter.

---

## Screen 11: Git Asks for Password

Terminal shows:
```
Password for 'https://surajuniyal073@github.com': 
```

**Paste your token here:**
```
Right-click or Cmd+V to paste your token
Password for 'https://surajuniyal073@github.com': ghp_1234567890abcdefghijklmnopqrstuvwxyz
```

Then press Enter.

---

## Screen 12: Push Completes

Terminal shows:
```
Enumerating objects: 15, done.
Counting objects: 100% (15/15), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (15/15), 200.00 KiB | 1.50 MiB/s, done.
Total 15 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'main' on GitHub by visiting:
remote:      https://github.com/surajuniyal073/assignment2_Converstational_AI/pull/new/main
remote:
To https://github.com/surajuniyal073/assignment2_Converstational_AI.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

**✅ Success! Your code is on GitHub!**

---

## Screen 13: Verify on GitHub

Open browser:
```
https://github.com/surajuniyal073/assignment2_Converstational_AI
```

You should see:
```
┌─────────────────────────────────────────────────────────┐
│ surajuniyal073 / assignment2_Converstational_AI          │
├─────────────────────────────────────────────────────────┤
│                                                         │
│ Intelligent Multi-Agent RAG System                      │
│                                                         │
│ ┌─────────────────────────────────────────────────────┐│
│ │ main  • 5 commits  • 1 branch                       ││
│ └─────────────────────────────────────────────────────┘│
│                                                         │
│ Files:                                                  │
│ ✅ .gitignore                                          │
│ ✅ AUTHENTICATION_NEEDED.md                            │
│ ✅ EVALUATION_MATRIX.md                               │
│ ✅ GITHUB_PUSH_GUIDE.md                               │
│ ✅ GITHUB_READY.md                                    │
│ ✅ GITHUB_TOKEN_GUIDE.md                              │
│ ✅ IMPLEMENTATION_GUIDE.md                            │
│ ✅ Multi_Agent_RAG_System.ipynb                       │
│ ✅ PUSH_NOW.md                                        │
│ ✅ QUICK_REFERENCE.md                                 │
│ ✅ README.md                                          │
│ ✅ START_HERE.md                                      │
│ ✅ assignment2.docx                                   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

All your files are there! ✅

---

## Summary of Steps

```
1. Go to GitHub settings
   👉 https://github.com/settings

2. Click Developer settings → Personal access tokens

3. Click "Generate new token (classic)"

4. Fill in:
   - Name: Conversational_AI_Push
   - Expiration: 90 days
   - Check: ✅ repo

5. Click "Generate token"

6. COPY the token (starts with ghp_)

7. In Terminal:
   git config --global credential.helper osxkeychain
   git push -u origin main

8. When asked:
   - Username: surajuniyal073
   - Password: [Paste your token]

9. ✅ Done! Check GitHub to verify
```

---

## Quick Command Summary

```bash
# Step 1: Configure credentials manager
git config --global credential.helper osxkeychain

# Step 2: Push your code
cd /Users/surajuniyal/Desktop/Conversational_AI
git push -u origin main

# Step 3: Enter credentials when prompted
# Username: surajuniyal073
# Password: [Paste your GitHub token]

# Step 4: Verify
# Go to: https://github.com/surajuniyal073/assignment2_Converstational_AI
```

---

## Expected Timing

- Generate token: 2 minutes
- Configure git: 30 seconds
- Push code: 2 minutes
- Verify on GitHub: 1 minute

**Total: ~5-6 minutes**

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Can't find Settings | Click your profile icon (top right) |
| Can't find Developer Settings | Scroll to bottom of Settings page left sidebar |
| Token disappeared after creation | Normal - you can only see it once. Delete and create new. |
| "Authentication failed" | Make sure you copied the entire token (all characters) |
| "Could not read Username" | Run credential helper first: `git config --global credential.helper osxkeychain` |
| Still asking for password | That's OK! First time it asks, then remembers. Try another push. |

---

## You're Ready! 🚀

Everything is set up. Just follow the steps above and your code will be on GitHub!

---

*Need help? See GITHUB_TOKEN_GUIDE.md for detailed explanations*
