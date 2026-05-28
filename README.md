# HoyoSophonDL

**HoyoSophonDL** is a Python-based tool that replicates and simplifies the core functionality of HoYoPlay's internal downloader systems — inspired by  
[Hi3Helper.Sophon](https://github.com/CollapseLauncher/Hi3Helper.Sophon) and [SophonDownloader](https://github.com/Escartem/SophonDownloader).

It supports both **CLI** and **GUI** modes, allowing users to download and manage HoYoPlay game assets efficiently.

---

## 🎯 Goal & Purpose

**HoyoSophonDL** is a **Python-native reimplementation** of HoYoPlay’s internal downloader logic.  
Its primary goals are to:

- Provide a **lightweight**, **cross-platform**, and **open-source** downloader for HoYoPlay assets.  
- Offer both a **command-line interface (CLI)** and a **PyQt6 GUI** for convenience.  
- Enable **multi-threaded**, **resumable**, and **cancelable** downloads.  
- Simplify asset management, manifest parsing, and patch version handling.

> ⚠️ **Disclaimer:**  
> This is an **unofficial third-party tool** unaffiliated with HoYoverse or Cognosphere.  
> It is designed purely for **educational and experimental purposes**.

---

## 🚀 Features

- 🧩 **CLI downloader** with progress tracking via `rich`
- 🖥️ **PyQt6 GUI** with progress bars, pause/resume/cancel controls
- ⚙️ Multi-threaded downloads using `ThreadPoolExecutor`
- 💾 Automatic resume via lightweight SQLite tracking
- 🔄 Asset validation and integrity checks
- 📦 Optional standalone `.exe` builder (Windows)

---

## 🧩 Installation

### Option 1 — Install from GitHub
If the package isn’t yet on PyPI, you can install it directly:
```bash
pip install git+https://github.com/Jo0X01/HoyoSophonDL.git
```

Or clone and install manually:
```bash
git clone https://github.com/Jo0X01/HoyoSophonDL.git
cd HoyoSophonDL
pip install .
```

### Option 2 — Install from PyPI *(after publishing)*
#### CLI-only (lightweight):

```bash
pip install HoyoSophonDL
```

#### With GUI (PyQt6) support:

```bash
pip install HoyoSophonDL[gui]
```

If you plan to build an executable:
```bash
pip install auto-py-to-exe
```

---

## 🧠 Usage

### CLI Mode
```bash
python -m HoyoSophonDL <game_name> [options]
```

#### Common Options

| Flag | Description |
|------|--------------|
| `-l, --list` | List all available games |
| `-i, --info` | Show game info |
| `-ai, --asset-info` | Show asset info |
| `-d, --download` | Start downloading selected assets |
| `-c, --category` | Asset category (default: `game`) |
| `-V, --current` | Current version |
| `-U, --update` | Target update version |
| `-o, --output` | Output directory |
| `-t, --threads` | Number of download threads |
| `-g, --gui` | Launch PyQt6 GUI instead of CLI |

#### Example
```bash
python -m HoyoSophonDL "Honkai Impact 3rd" -d -c game -o ./downloads -t 20
```

### GUI Mode
```bash
python -m HoyoSophonDL --gui
```

---

## 🏗️ Building Executables (Windows)

You can turn your Python project into a standalone `.exe` using **auto-py-to-exe**

---

## 🧱 Architecture Target

Your build’s architecture (x86 or x64) depends on your **Python interpreter**:
- To build **x64**, use 64-bit Python.
- To build **x86**, install 32-bit Python and rebuild.

---

## ⚖️ License

This project is licensed under the **GNU General Public License v3.0 (GPLv3)**.

---

## 🧾 Credits

- [Hi3Helper.Sophon](https://github.com/CollapseLauncher/Hi3Helper.Sophon)  
- [SophonDownloader](https://github.com/Escartem/SophonDownloader)  
- [Rich](https://github.com/Textualize/rich)  
- [PyQt6](https://pypi.org/project/PyQt6/)

---

## 🧩 Author

Developed by **Mr.Jo0x01**  
For learning, research, and open-source contribution.
