# 🪟 Windows Execution Guide - Multi-Agent RAG System

## Complete Step-by-Step Guide to Run on Windows

---

## PART 1: SYSTEM REQUIREMENTS

### What You Need:
- ✅ Windows 10 or Windows 11
- ✅ At least 4GB RAM (8GB recommended)
- ✅ 2GB free disk space
- ✅ Administrator access (for installation)
- ✅ Internet connection

---

## PART 2: INSTALL PYTHON

### Step 1: Download Python

1. Go to: https://www.python.org/downloads/
2. Click **Download Python 3.9** or higher (3.10, 3.11 also work)
3. Choose **Windows installer (64-bit)** version

### Step 2: Install Python

1. Run the downloaded installer
2. ⚠️ **IMPORTANT:** Check the box: **"Add Python to PATH"**
3. Click **Install Now**
4. Wait for installation to complete
5. Click **Close**

### Step 3: Verify Python Installation

Open **Command Prompt** (Press: Windows + R, type `cmd`, press Enter)

Type:
```cmd
python --version
```

You should see:
```
Python 3.9.x (or higher)
```

If you see this, Python is installed correctly! ✅

---

## PART 3: INSTALL GIT (Optional but Recommended)

### Step 1: Download Git

1. Go to: https://git-scm.com/download/win
2. Click the installer for 64-bit Windows
3. Run the installer

### Step 2: Install Git

1. Click through the installer
2. Use default settings
3. Click **Install**
4. Click **Finish**

### Step 3: Verify Git Installation

Open **Command Prompt**

Type:
```cmd
git --version
```

You should see Git version number ✅

---

## PART 4: CLONE YOUR REPOSITORY (Two Options)

### OPTION A: Using Git (Recommended)

Open **Command Prompt** and run:

```cmd
git clone https://github.com/surajuniyal073/assignment2_Converstational_AI.git
cd assignment2_Converstational_AI
```

This downloads all your code to a folder.

### OPTION B: Without Git

1. Go to: https://github.com/surajuniyal073/assignment2_Converstational_AI
2. Click **Code** (green button)
3. Click **Download ZIP**
4. Extract the ZIP file
5. Open Command Prompt in that folder

---

## PART 5: SET UP PYTHON ENVIRONMENT

### Step 1: Navigate to Project Folder

Open **Command Prompt** and type:

```cmd
cd path\to\assignment2_Converstational_AI
```

Replace `path\to\` with your actual path.

**Example:**
```cmd
cd C:\Users\YourName\Downloads\assignment2_Converstational_AI
```

### Step 2: Create Virtual Environment

Type this command:

```cmd
python -m venv venv
```

This creates a virtual environment (isolated Python setup for your project).

### Step 3: Activate Virtual Environment

Type:

```cmd
venv\Scripts\activate
```

You should see `(venv)` at the beginning of your prompt:

```
(venv) C:\Users\YourName\...\assignment2_Converstational_AI>
```

✅ Virtual environment is now active!

---

## PART 6: INSTALL DEPENDENCIES

### Install All Required Libraries

With virtual environment activated, type:

```cmd
pip install -r requirements.txt
```

If `requirements.txt` doesn't exist, install manually:

```cmd
pip install numpy pandas scikit-learn torch transformers sentence-transformers faiss-cpu langchain openai python-docx PyPDF2 pydantic networkx matplotlib seaborn
```

⏱️ This may take 5-10 minutes. Wait for it to complete.

When done, you'll see:
```
Successfully installed ...
```

✅ All dependencies are installed!

---

## PART 7: START JUPYTER NOTEBOOK

### Step 1: Launch Jupyter

With virtual environment still active, type:

```cmd
jupyter notebook
```

### Step 2: Wait for Jupyter to Start

You should see:
```
Jupyter Notebook 6.x.x is running at:
http://localhost:8888/?token=...
```

Your browser should automatically open to Jupyter.

If not, go to: http://localhost:8888

---

## PART 8: OPEN YOUR PROJECT NOTEBOOK

### Step 1: Navigate in Jupyter

In Jupyter browser window:
1. You should see the project folder contents
2. Look for: **Multi_Agent_RAG_System.ipynb**
3. Click on it to open

### Step 2: Run the Notebook

The notebook is now open. You'll see cells of code.

Run each cell in order:

1. **Click on the first cell** (in the code area)
2. **Press Ctrl + Enter** to execute
3. **Wait for it to complete**
4. Move to next cell and repeat

Or use the menu:
- Click **Cell** → **Run All** to run everything at once

---

## PART 9: WHAT EACH SECTION DOES

### Setup Section (Cells 1-2)
- ✅ Installs dependencies
- ✅ Imports all libraries
- **Expected time:** 2-5 minutes

### Task 1: Indexing (Cells 3-7)
- ✅ Document processing
- ✅ Creates 4 indexing strategies
- ✅ Compares retrieval methods
- **Expected time:** 3-5 minutes

### Task 2: Agents (Cells 8-12)
- ✅ Creates 5 specialized agents
- ✅ Demonstrates collaboration
- ✅ Unifies evidence
- **Expected time:** 2-3 minutes

### Task 3: Verification (Cells 13-17)
- ✅ Verifies evidence quality
- ✅ Computes trust scores
- ✅ Optimizes context
- **Expected time:** 2-3 minutes

### Task 4: Adaptation (Cells 18-22)
- ✅ Classifies queries
- ✅ Demonstrates adaptive retrieval
- **Expected time:** 2-3 minutes

### Task 5: Evaluation (Cells 23-30)
- ✅ Calculates metrics
- ✅ Robustness testing
- ✅ Monitoring dashboard
- **Expected time:** 3-5 minutes

---

## PART 10: TROUBLESHOOTING

### Problem: Python not found

**Solution:**
1. Reinstall Python
2. Make sure "Add Python to PATH" is checked
3. Restart Command Prompt
4. Try again

### Problem: pip command not found

**Solution:**
```cmd
python -m pip install package_name
```

### Problem: Virtual environment not activating

**Solution:**
Try this instead of `venv\Scripts\activate`:

```cmd
python -m venv venv
python -m venv\Scripts\activate.bat
```

### Problem: Jupyter notebook command not found

**Solution:**
```cmd
python -m jupyter notebook
```

### Problem: Out of memory error

**Solution:**
1. Close other applications
2. Reduce number of chunks in Task 1
3. Restart Jupyter

### Problem: Import errors (e.g., "No module named 'torch'")

**Solution:**
```cmd
pip install torch transformers sentence-transformers
```

### Problem: Dependencies installation takes too long

**Solution:**
- This is normal (5-10 minutes)
- Don't close the window
- Let it complete
- Some packages are large (PyTorch, etc.)

---

## PART 11: COMPLETE WINDOWS WORKFLOW

### Quick Copy-Paste Steps:

```cmd
REM Step 1: Clone repository
git clone https://github.com/surajuniyal073/assignment2_Converstational_AI.git
cd assignment2_Converstational_AI

REM Step 2: Create virtual environment
python -m venv venv

REM Step 3: Activate virtual environment
venv\Scripts\activate

REM Step 4: Install dependencies
pip install numpy pandas scikit-learn torch transformers sentence-transformers faiss-cpu langchain openai python-docx PyPDF2 pydantic networkx matplotlib seaborn

REM Step 5: Start Jupyter
jupyter notebook
```

Then in Jupyter browser:
1. Open `Multi_Agent_RAG_System.ipynb`
2. Run all cells
3. See your results! ✅

---

## PART 12: EXPECTED OUTPUTS

### Task 1 Output:
```
✓ Processed technical_manual.txt: 2 chunks
✓ Processed compliance_policy.txt: 2 chunks
✓ Vector index built with 6 chunks
✓ Keyword index built with 6 chunks
```

### Task 2 Output:
```
[Policy Retrieval Agent] Retrieving...
  Retrieved 5 results
Total Evidence Items: 25
```

### Task 3 Output:
```
Verified 25 evidence items
Trust Score: 0.600-0.950
Optimized Context Window
```

### Task 4 Output:
```
Query Classification: MULTI_HOP (confidence: 0.85)
Total Evidence Found: 5-15
```

### Task 5 Output:
```
Retrieval Metrics:
  Recall@5: 0.75
  Precision@5: 0.85
  nDCG@5: 0.88
```

---

## PART 13: RUNNING INDIVIDUAL TASKS

If you want to run just one task:

### Run Only Task 1:
```python
# Execute cells 1-2 (setup)
# Then execute cells 3-7 (Task 1)
```

### Run Task 1 + Task 2:
```python
# Execute cells 1-2 (setup)
# Execute cells 3-7 (Task 1)
# Execute cells 8-12 (Task 2)
```

---

## PART 14: SAVE YOUR WORK

### Export Notebook as PDF:

In Jupyter:
1. Click **File** menu
2. Click **Export Notebook As**
3. Select **PDF via LaTeX** or **HTML**
4. Choose save location
5. File is saved! ✅

---

## PART 15: IMPORTANT NOTES

⚠️ **First Run Warnings:**

1. **Dependencies take time:** Don't worry if installation takes 5-10 minutes. This is normal, especially for PyTorch and large packages.

2. **First cell execution:** First cell may take 1-2 minutes as it imports all libraries.

3. **Vector embeddings:** Task 1 may take 2-3 minutes to compute embeddings. This is normal.

4. **Large files:** Some operations process large amounts of data. Be patient.

5. **Memory usage:** The notebook may use 500MB-1GB RAM during execution. Make sure you have enough.

---

## PART 16: QUICK REFERENCE

| Task | Time | What It Does |
|------|------|-------------|
| Setup | 3-5 min | Install dependencies |
| Task 1 | 3-5 min | Document processing |
| Task 2 | 2-3 min | Multi-agent retrieval |
| Task 3 | 2-3 min | Evidence verification |
| Task 4 | 2-3 min | Adaptive retrieval |
| Task 5 | 3-5 min | Evaluation metrics |
| **TOTAL** | **20-30 min** | Full execution |

---

## PART 17: AFTER SUCCESSFUL EXECUTION

✅ You have successfully:
- Downloaded your code from GitHub
- Set up Python environment
- Installed all dependencies
- Executed all 5 tasks
- Seen the complete RAG system in action!

Now you can:
- ✅ Share your results
- ✅ Modify the code
- ✅ Run individual tasks
- ✅ Export as PDF
- ✅ Use as reference

---

## FINAL CHECKLIST

Before starting, make sure you have:

- [ ] Windows 10 or 11
- [ ] 4GB+ RAM free
- [ ] 2GB+ disk space
- [ ] Python 3.9+ installed
- [ ] Git installed (optional)
- [ ] Internet connection

During execution, you should see:

- [ ] Python version confirmed
- [ ] Virtual environment activated
- [ ] Dependencies installed successfully
- [ ] Jupyter started
- [ ] Notebook opened
- [ ] All cells executing
- [ ] Results displayed

After execution:

- [ ] All 5 tasks completed
- [ ] Outputs shown in notebook
- [ ] No errors (or only warnings)
- [ ] Can export as PDF
- [ ] Results saved

---

## SUPPORT & HELP

### If you get stuck:

1. **Read the error message carefully**
2. **Google the error** - usually has solutions
3. **Check troubleshooting section** above
4. **Try again** - sometimes just needs retry
5. **Ask for help** - copy the error message

### Common Error Messages:

| Error | Solution |
|-------|----------|
| "python: command not found" | Reinstall Python with "Add to PATH" |
| "No module named 'torch'" | Run: `pip install torch` |
| "Permission denied" | Open Command Prompt as Administrator |
| "Port 8888 already in use" | Change port: `jupyter notebook --port 8889` |
| "Out of memory" | Close other apps, restart |

---

## CONGRATULATIONS! 🎉

You have everything needed to run the Multi-Agent RAG System on Windows!

Follow the steps above and you'll have it running in ~30 minutes.

Good luck! 🚀

---

**Need help?** 
- Check the documentation files in your repository
- Read inline comments in the notebook
- Try running cells one by one
- Share the error message if stuck

**Happy coding!** 💻
