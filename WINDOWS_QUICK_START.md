# ⚡ Windows Quick Start (30 Minutes)

## Copy-Paste These Commands in Order

### Step 1: Clone Repository (1 minute)

Open **Command Prompt** and paste:

```cmd
git clone https://github.com/surajuniyal073/assignment2_Converstational_AI.git
cd assignment2_Converstational_AI
```

### Step 2: Create Virtual Environment (30 seconds)

```cmd
python -m venv venv
```

### Step 3: Activate Virtual Environment (5 seconds)

```cmd
venv\Scripts\activate
```

You should see `(venv)` in your command prompt.

### Step 4: Install All Dependencies (5-10 minutes)

```cmd
pip install --upgrade pip
pip install numpy pandas scikit-learn torch transformers sentence-transformers faiss-cpu langchain openai python-docx PyPDF2 pydantic networkx matplotlib seaborn jupyter
```

### Step 5: Start Jupyter Notebook (10 seconds)

```cmd
jupyter notebook
```

Your browser should open automatically. If not, go to: **http://localhost:8888**

### Step 6: Open the Notebook

In Jupyter:
1. Click: `Multi_Agent_RAG_System.ipynb`
2. Notebook opens

### Step 7: Run All Cells

In Jupyter menu:
1. Click: **Cell**
2. Click: **Run All**

Or run individually:
1. Click on a cell
2. Press: **Ctrl + Enter**
3. Repeat for each cell

### Step 8: Wait for Completion (15-20 minutes)

Watch the output. Each task will show:
- ✅ Task progress
- ✅ Results
- ✅ Metrics

Done! 🎉

---

## ALL COMMANDS IN ONE BLOCK

Copy and paste everything at once:

```cmd
git clone https://github.com/surajuniyal073/assignment2_Converstational_AI.git
cd assignment2_Converstational_AI
python -m venv venv
venv\Scripts\activate
pip install --upgrade pip
pip install numpy pandas scikit-learn torch transformers sentence-transformers faiss-cpu langchain openai python-docx PyPDF2 pydantic networkx matplotlib seaborn jupyter
jupyter notebook
```

---

## WHAT TO EXPECT

### Installation (5-10 minutes)
```
Collecting numpy...
Collecting pandas...
...
Successfully installed [many packages]
```

### Starting Jupyter
```
Jupyter Notebook 6.4.12 is running at:
http://localhost:8888/?token=...
```

### Running Tasks
```
✓ Processed technical_manual.txt: 2 chunks
✓ Vector index built with 6 chunks
...
[Task outputs shown]
```

---

## TROUBLESHOOTING - QUICK FIXES

### Python not installed?
→ Download from https://www.python.org/downloads/
→ Run installer with "Add Python to PATH" checked

### Git not installed?
→ Download from https://git-scm.com/download/win
→ Or download ZIP manually from GitHub

### Virtual environment not activating?
→ Try: `python -m venv venv` then `venv\Scripts\activate.bat`

### Dependencies installation fails?
→ Run: `pip install --upgrade pip`
→ Then try installation again

### Jupyter not starting?
→ Try: `python -m jupyter notebook`

### Port 8888 in use?
→ Try: `jupyter notebook --port 8889`

---

## TIME BREAKDOWN

| Step | Time |
|------|------|
| Clone repository | 1 min |
| Create venv | 30 sec |
| Activate venv | 5 sec |
| Install dependencies | 5-10 min |
| Start Jupyter | 10 sec |
| Open notebook | 10 sec |
| Run all cells | 15-20 min |
| **TOTAL** | **~30 minutes** |

---

## SYSTEM REQUIREMENTS

- ✅ Windows 10/11
- ✅ 4GB RAM (8GB recommended)
- ✅ 2GB free disk space
- ✅ Internet connection
- ✅ Administrator access for installation

---

## FINAL CHECK

After running:

✅ All 5 tasks completed
✅ Outputs shown in notebook
✅ No fatal errors
✅ Results displayed
✅ Ready to export as PDF

---

**That's it! Your code is running on Windows! 🎉**

For detailed guide, see: `WINDOWS_EXECUTION_GUIDE.md`

Happy coding! 🚀
