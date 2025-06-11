
---

# MindsDB Installation Guide – For Developers & Users (Windows Native / Source)

---

## What is MindsDB?

**MindsDB** is an open-source platform that lets you create, train, and deploy machine learning models using SQL. It supports:

* Structured data from CSV, Excel, or databases
* Predictive modeling using simple SQL
* Integrations with MySQL, PostgreSQL, MongoDB, and more
* Use cases like LLMs, Chatbots, Time Series, and Classification

---

## Choose Your Installation Path

| Use Case                                    | Recommended Setup                                                              |
| ------------------------------------------- | ------------------------------------------------------------------------------ |
| I want to try MindsDB quickly on Windows    | [Native Python Install (no Docker)](#install-mindsdb-on-windows---no-docker) |
| I want to contribute to MindsDB development | [Install from Source](#install-mindsdb-from-source---for-development)    |

---

## Install MindsDB on Windows — No Docker

This method is perfect if you're a beginner and want to use MindsDB locally without Docker.

### ✅ Requirements

| Tool   | Version                        |
| ------ | ------------------------------ |
| Python | 3.10.x or 3.11.x (avoid 3.12+) |
| pip    | Comes with Python              |
| Git    | (Optional) For advanced usage  |

---

### Step 1: Install Python

1. Download from [python.org](https://www.python.org/downloads/)
2. Run the installer:

   * ✅ Check **"Add Python to PATH"**
   * Click **Install Now**

---

### Step 2: Verify Installation

```bash
python --version
pip --version
```

---

### Step 3: Create and Activate Virtual Environment

```bash
cd C:\Users\YourUsername\Documents
mkdir MindsDB && cd MindsDB
python -m venv mindsdb_env
.\mindsdb_env\Scripts\activate
```

You’ll see:

```
(mindsdb_env) C:\Users\YourUsername\Documents\MindsDB>
```

---

### Step 4: Upgrade Tools and Install MindsDB

```bash
python -m pip install --upgrade pip setuptools wheel
pip install mindsdb
```

---

### Step 5: Run MindsDB

```bash
python -m mindsdb
```

You should see:

```
INFO    MindsDB API running on http://127.0.0.1:47334
INFO    MindsDB Studio running on http://127.0.0.1:47335
```

Open your browser at: [http://127.0.0.1:47335](http://127.0.0.1:47335)

---

## Install MindsDB from Source — For Development

If you're planning to **contribute to MindsDB**, install it from source with development tools.

---

### ⚙️ Developer Setup Requirements

* Python 3.10.x or 3.11.x
* Git
* pip + virtualenv

---

### Step-by-Step:

1. **Fork MindsDB on GitHub**
   👉 [https://github.com/mindsdb/mindsdb](https://github.com/mindsdb/mindsdb)

2. **Clone your fork locally:**

   ```bash
   git clone https://github.com/<your-username>/mindsdb.git
   cd mindsdb
   ```

3. **Create a virtual environment:**

   ```bash
   python -m venv mindsdb-venv
   ```

4. **Activate the virtual environment:**

   * **Windows:**

     ```bash
     .\mindsdb-venv\Scripts\activate
     ```
   * **macOS/Linux:**

     ```bash
     source mindsdb-venv/bin/activate
     ```

5. **Install MindsDB and dev dependencies:**

   ```bash
   pip install -e .
   pip install -r requirements/requirements-dev.txt
   ```

6. **Run MindsDB:**

   ```bash
   python -m mindsdb
   ```

---

### Advanced Options

* **Start with specific APIs:**

  ```bash
  python -m mindsdb --api http,mysql,postgres,mongodb
  ```

* **Disable Studio (GUI):**

  ```bash
  python -m mindsdb --no_studio
  ```

* **Using Makefile (Optional):**

  ```bash
  make install_mindsdb
  make run_mindsdb
  ```

---

## Install Additional Integrations

To install optional dependencies for specific data or ML integrations:

```bash
pip install .[handler_name]
```

🔗 [List of all handlers](https://github.com/mindsdb/mindsdb/tree/main/mindsdb/integrations/handlers)

---

## What’s Next?

Now that you’ve installed MindsDB, try:

* [`CREATE MODEL`](/sql/create/model) – to train models using SQL
* [Use Cases](/use-cases/overview) – tutorials for LLMs, Time Series, Regression, etc.

---

## You're Ready!

Whether you're building your first predictive model or contributing to MindsDB itself, you're now set up and ready to go. Happy hacking! 

---


