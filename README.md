# 🏛️ Auction House Data Analysis — Getting Started

This notebook explores auction sales, buyer behaviour, and catalog pricing across a series of art and collectibles auctions. It is designed to guide you through the early analysis and then leave you to explore further.

---

## Getting the Files

Everything you need — the notebook and both data files — is in one GitHub repository:

**[https://github.com/Isabellemehigan/inHouseDayDataAnalysis](https://github.com/Isabellemehigan/inHouseDayDataAnalysis)**

You can get the files in two ways:

**Download as a ZIP (no Git required)**
1. Click the green **Code** button on the GitHub page
2. Click **Download ZIP**
3. Unzip the folder — all three files will be inside

**Clone with Git (if you have Git installed)**
```bash
git clone https://github.com/Isabellemehigan/inHouseDayDataAnalysis.git
cd inHouseDayDataAnalysis
```

The repo contains:
```
auction_analysis.ipynb
Auctions_and_contacts__1_.xlsx
Full_Catalog__1_.xlsx
Financial_transactions.xlsx
IzzyAuctionHouse_Case_Database.db
```

---

## Option 1 — Google Colab

Google Colab runs entirely in your browser with no installation required. It can open the notebook directly from GitHub.

**Fastest way — open directly from GitHub:**
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Open notebook → GitHub**
3. Paste in the repo URL:
   ```
   https://github.com/Isabellemehigan/inHouseDayDataAnalysis
   ```
4. Select `auction_analysis.ipynb` from the list

**Then upload the data files.** You have two options:

**Option A — Upload directly (simpler, files lost when session ends)**
- Click the 📁 folder icon in the left sidebar
- Click the upload icon (page with an arrow) and upload both `.xlsx` files from your downloaded ZIP
- The files will appear at `/content/` which is where the notebook looks by default

**Option B — Mount Google Drive (files persist between sessions)**
- Upload the three `.xlsx` files to your Google Drive first
- Add this cell at the top of the notebook and run it:
  ```python
  from google.colab import drive
  drive.mount('/content/drive')
  ```
- Then update the file paths in the **Load the Data** cell to point to your Drive folder e.g.:
  ```python
  items   = pd.read_excel('/content/drive/MyDrive/inHouseDayDataAnalysis/Auctions_and_contacts.xlsx', sheet_name='Auction Items')
  catalog = pd.read_excel('/content/drive/MyDrive/inHouseDayDataAnalysis/Full_Catalog.xlsx', sheet_name='Full Catalog')
  ```

5. Click **Runtime → Run all** to execute every cell, or use **Shift + Enter** to run one cell at a time.
---

## Option 2 — Kaggle Notebooks

Kaggle Notebooks are free and can also pull directly from GitHub.

1. Go to [kaggle.com](https://www.kaggle.com) and sign in (free account required)
2. Click **Create → New Notebook**
3. Click **File → Import notebook** and paste the GitHub URL:
   ```
   https://github.com/Isabellemehigan/inHouseDayDataAnalysis
   ```
   Then select `auction_analysis.ipynb`
4. Add the data files:
   - In the right-hand panel click **+ Add data → Upload**
   - Upload both `.xlsx` files from your downloaded ZIP
   - Kaggle places them at `/kaggle/input/<dataset-name>/`
   ```
5. Click **Run All** or use **Shift + Enter** cell by cell.

> **Tip:** You can make your Kaggle notebook public and share the link — useful for submitting work or collaborating.

---

## Option 3 — Running Locally

Running locally gives you the most control and everything stays on your machine.

### Step 1 — Get the files

Clone or download the repo as described in **Getting the Files** above.

### Step 2 — Install Python

If you do not have Python installed, download it from [python.org](https://www.python.org/downloads/) (version 3.9 or higher recommended). On Windows, check **Add Python to PATH** during installation.

### Step 3 — Install the required libraries

Open a terminal (Mac/Linux) or Command Prompt (Windows) and run:

```bash
pip install jupyter pandas matplotlib seaborn openpyxl
```

### Step 4 — Launch Jupyter

Navigate into the repo folder and start Jupyter:

```bash
cd inHouseDayDataAnalysis
jupyter notebook
```

## Option 4 — SQL on SQLite 

SQLite is a free online SQL IDE.

1. Download the repo zip folder as described above
2. Go to [sqlite.com](https://sqliteonline.com)
3. Add the data files:
   - In the top-left panel click the **Database icon → Open SQLite DB**
   - Upload  `IzzyAuctionHouse_Case_Database.db` from your downloaded ZIP
---
