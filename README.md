# MindsDB Native Python Installation on Windows (No Docker) — Step-by-Step Tutorial

---

## What is MindsDB?

**MindsDB** is a tool that allows you to create and use machine learning models using **SQL-like syntax**. You can:

- Train models from CSV/Excel files
- Predict outcomes from your data
- Connect to databases like MySQL, PostgreSQL, MongoDB, etc.

---

## Requirements

Before installing MindsDB, make sure your system has:

| Tool                | Required Version      |
| ------------------- | --------------------- |
| Python              | 3.8 to 3.11           |
| pip                 | Installed with Python |
| Git (Optional)      | For advanced use      |

---

## Step 1: Install Python on Windows

1. Go to: 👉 [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Download Python 3.11.x or 3.10.x (Avoid 3.12+ for now)
3. Run the installer:

   - ✅ Make sure to **check the box**: “Add Python to PATH”
   - Click **Install Now**

---

## Step 2: Verify Installation

Open **Command Prompt** or **PowerShell**, and type:

```bash
python --version
pip --version
```

You should see something like:

```
Python 3.11.x
pip 23.x.x
```

If you see an error, Python was not installed correctly or not added to PATH.

---

## Step 3: Create a Virtual Environment (Recommended)

Virtual environments keep your projects clean and avoid version conflicts.

```bash
# Go to your desired folder (e.g., Documents)
cd C:\Users\YourUsername\Documents

# Create a folder for MindsDB
mkdir MindsDB
cd MindsDB

# Create a virtual environment
python -m venv mindsdb_env

# Activate it
.\mindsdb_env\Scripts\activate
```

Once activated, your command prompt will look like:

```
(mindsdb_env) C:\Users\YourUsername\Documents\MindsDB>
```

---

## Step 4: Upgrade pip, setuptools, and wheel

This step ensures smooth installation.

```bash
python -m pip install --upgrade pip setuptools wheel
```

---

## Step 5: Install MindsDB

Now install MindsDB using pip:

```bash
pip install mindsdb
```

This may take a few minutes — it installs machine learning libraries in the background.

---

## Step 6: Run MindsDB

⚠️ Important: On Windows, the `mindsdb` command might not work directly, so use this instead:

```bash
python -m mindsdb
```

If successful, you’ll see:

```
INFO    MindsDB API running on http://127.0.0.1:47334
INFO    MindsDB Studio running on http://127.0.0.1:47335
```

---

## Step 7: Open MindsDB Studio in Browser

Open your browser and go to:

```
http://127.0.0.1:47335
```

You’ll see the MindsDB interface where you can:

- Upload datasets
- Create machine learning models
- Make predictions

---


## You're All Set!

You now have **MindsDB fully running natively on Windows** — no Docker, no virtual machines, just clean Python. 

---
