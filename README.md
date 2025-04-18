# 🐍 Python Environment Setup with uv + Jupyter Notebook (Linux & Windows)

This guide explains how to:

- Install Python and pip
- Install [`uv`](https://github.com/astral-sh/uv) for fast virtual environments
- Create and activate a virtual environment
- Install and run Jupyter Notebook
- Test with a simple example

---

## 📦 Requirements

- Python 3.x
- Internet access

---

## 🐧 Linux (Ubuntu/Debian)

### ✅ 1. Install Python and pip
```bash
sudo apt update
sudo apt install python3 python3-pip -y
```

### ✅ 2. Install uv
```bash
curl -Ls https://astral.sh/uv/install.sh | bash
```

Add to path:
```bash
echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Verify:
```bash
uv --version
```

### ✅ 3. Create and activate virtual environment
```bash
uv venv bn
source bn/bin/activate
```

### ✅ 4. Install Jupyter Notebook
```bash
pip install notebook
```

### ✅ 5. Run Jupyter
```bash
jupyter notebook
```

Open browser: http://localhost:8888/tree

---

## 🪟 Windows (CMD or PowerShell)

### ✅ 1. Install Python and pip
Download from: https://www.python.org/downloads/

Enable ✅ "Add Python to PATH" during installation.

Check:
```bash
python --version
pip --version
```

### ✅ 2. Install uv
Use PowerShell:
```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

Check:
```bash
uv --version
```

### ✅ 3. Create and activate virtual environment
```bash
uv venv bn
.\bn\Scripts\activate
```

### ✅ 4. Install Jupyter Notebook
```bash
pip install notebook
```

### ✅ 5. Run Jupyter Notebook
```bash
jupyter notebook
```

---

## 📓 Sample Jupyter Notebook
In browser, click New → Python 3 Notebook

Paste this in the cell:
```python
print("Hello from Jupyter!")
```
Press Shift + Enter to run

---

## 🧠 Tips
To deactivate the venv:
```bash
deactivate
```

To remove the virtual environment:
```bash
rm -rf bn  # Linux/macOS
rmdir /s /q bn  # Windows
```
