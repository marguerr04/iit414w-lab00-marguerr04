# (a) Header - Lab 0 — Reproducible Setup & FastF1 Sanity Check

## IIT414W · Unit I · March 2026

**Student:** Martín Isaias Guerrero Ancapichún
**GitHub:** marguerr04  
**Course:** IIT414W — Artificial Intelligence Workshop  
**Date:** March 11, 2026

---

## (b) System Info

| Component        | Version / Detail                                      |
|------------------|-------------------------------------------------------|
| Operating System | Windows 11 Home Single Language (10.0.26200, Long Paths enabled) |
| Python           | 3.13.7 (newer than the course reference 3.10; documented intentionally) |
| pip              | 25.2                                                  |
| Git              | 2.45.1                                                |
| Environment      | `venv` + `pip` (no conda)                             |

---

## (c) Setup Instructions

```powershell
# 1. Clone the repository
git clone https://github.com/marguerr04/iit414w-lab00-marguerr04.git
cd iit414w-lab00-marguerr04

# 2. Create a virtual environment
python -m venv .venv

# 3. Activate the virtual environment
# PowerShell:
.venv\Scripts\Activate.ps1
# CMD:
.venv\Scripts\activate.bat

# 4. Install all dependencies
pip install -r requirements.txt
```

---

## (d) How to Run

1. Open the project folder in **VS Code**.
2. Select the `.venv` Python interpreter as your Kernel (Ctrl+Shift+P → "Python: Select Interpreter" → choose the `.venv` one).
3. Run **`setup_check.ipynb`** first: Kernel → **Restart & Run All**.
4. Then run **`data_check.ipynb`**: Kernel → **Restart & Run All**.

> **Note:** The first execution of `data_check.ipynb` downloads F1 data from the internet and may take 1–3 minutes. Subsequent runs use the local cache.

---

## (e) Problems Encountered

### Problem 1 — `[Errno 2] No such file or directory` during `pip install`

**Error:** Running `pip install -r requirements.txt` failed with `[Errno 2] No such file or directory` on several packages. The root cause was the Windows 260-character path length limit — the deeply nested `.venv` path exceeded the OS maximum.

**Solution:** 

Cleaned `requirements.txt` to only list top-level dependencies (removed transitive sub-dependencies) and re-ran `pip install -r requirements.txt` successfully.

---

## (f) Expected Outputs

- **`setup_check.ipynb`**: Prints Python version, NumPy version, and `RANDOM_SEED = 414`. Displays the 6-package version table, working directory, FastF1 cache path, and Git version. All decision and reflection cells are filled with personal answers.
- **`data_check.ipynb`**: Loads the Bahrain 2024 Race session via FastF1, prints session name, event name, results shape, column names, and the first 5 laps. Queries the Jolpica API and displays HTTP 200 status, record count, and the first 3 drivers (Verstappen, Norris, Leclerc) with nationality and points.