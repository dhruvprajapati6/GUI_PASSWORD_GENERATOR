<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=320&color=0:050816,20:0f172a,45:312e81,70:7c3aed,100:0ea5e9&text=🔐%20SecurePass%20Pro&fontSize=56&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Ultra-Secure%20Password%20Generator%20for%20Modern%20Users&descAlignY=62&descSize=20"/>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&weight=700&size=26&duration=3000&pause=1000&color=A855F7&center=true&vCenter=true&width=800&lines=🔒+Generate+Military-Grade+Passwords;⚡+Fast+%7C+Secure+%7C+Modern;🛡️+Protect+Your+Digital+Identity;🚀+Built+with+Python+and+Passion" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0-8B5CF6?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Security-High-success?style=for-the-badge&logo=shield"/>
  <img src="https://img.shields.io/badge/Status-Active-22C55E?style=for-the-badge"/>
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/yourusername/SecurePass-Pro?style=for-the-badge&color=8B5CF6&label=Stars"/>
  <img src="https://img.shields.io/github/forks/yourusername/SecurePass-Pro?style=for-the-badge&color=0EA5E9&label=Forks"/>
  <img src="https://img.shields.io/badge/License-MIT-F59E0B?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/PRs-Welcome-22C55E?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Made%20with-%E2%9D%A4%EF%B8%8F%20%26%20Python-7C3AED?style=for-the-badge"/>
</p>

<p align="center">
  <a href="#-features"><img src="https://img.shields.io/badge/-Features-8B5CF6?style=for-the-badge"/></a>
  <a href="#-demo"><img src="https://img.shields.io/badge/-Demo-312e81?style=for-the-badge"/></a>
  <a href="#-installation"><img src="https://img.shields.io/badge/-Installation-0EA5E9?style=for-the-badge"/></a>
  <a href="#-usage"><img src="https://img.shields.io/badge/-Usage-22C55E?style=for-the-badge"/></a>
  <a href="#-security"><img src="https://img.shields.io/badge/-Security-EF4444?style=for-the-badge"/></a>
  <a href="#-contributing"><img src="https://img.shields.io/badge/-Contributing-F59E0B?style=for-the-badge"/></a>
</p>

</div>

<br>

## ✨ Features

| | Feature | Description |
|:---:|---|---|
| 🎲 | **Cryptographically Secure** | Built on Python's `secrets` module (CSPRNG) — not `random` |
| 📏 | **Custom Length** | Generate passwords anywhere from 4 to 128 characters |
| 🔤 | **Character Control** | Independently toggle uppercase, lowercase, digits, and symbols |
| 🚫 | **Ambiguous Character Filter** | Strip out confusing characters like `0`, `O`, `1`, `l`, `I` |
| 📊 | **Strength Meter** | Real-time entropy calculation with a clear strength rating |
| 📦 | **Bulk Generation** | Generate multiple passwords in a single command |
| 📋 | **Clipboard Copy** | Optional one-flag clipboard copy of the result |
| 🕵️ | **Zero Logging** | Nothing is ever written to disk, cached, or sent over a network |
| 🖥️ | **Cross-Platform** | Runs the same on Windows, macOS, and Linux |
| ⚡ | **Lightweight** | Pure Python core with minimal dependencies |

<br>

## 🖥️ Demo

```bash
$ python securepass.py --length 20 --count 3

╔══════════════════════════════════════════╗
║          🔐 SecurePass Pro v1.0           ║
╚══════════════════════════════════════════╝

Generated Passwords:
  1. xK9$mPz#4Qw&Rt2!aLbN
  2. Yh7*Vn3@uJk6%Wp9$Esz
  3. Bq2&Tm8!Lx5#Nf1@Gdw4

Strength : ⭐⭐⭐⭐⭐ Very Strong  (≈131-bit entropy)
Est. crack time (offline brute force): effectively uncrackable
```

<br>

## ⚙️ Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/SecurePass-Pro.git
cd SecurePass-Pro

# (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

<br>

## 🚀 Usage

```bash
# Generate a single 16-character password (default)
python securepass.py

# Generate a 24-character password without symbols
python securepass.py --length 24 --no-symbols

# Generate 5 passwords at once
python securepass.py --count 5

# Exclude ambiguous characters and copy result to clipboard
python securepass.py --exclude-ambiguous --copy
```

<div align="center">

| Flag | Description | Default |
|---|---|---|
| `--length`, `-l` | Password length | `16` |
| `--count`, `-c` | Number of passwords to generate | `1` |
| `--no-upper` | Exclude uppercase letters | `False` |
| `--no-lower` | Exclude lowercase letters | `False` |
| `--no-numbers` | Exclude digits | `False` |
| `--no-symbols` | Exclude special characters | `False` |
| `--exclude-ambiguous` | Remove confusing characters (`0 O 1 l I`) | `False` |
| `--copy` | Copy result to clipboard | `False` |

</div>

<br>

## 🔐 Security

SecurePass Pro is designed offline-first and audit-friendly:

- 🎯 Powered entirely by Python's `secrets` module — a CSPRNG meant for security-sensitive work, unlike the standard `random` module.
- 🌐 No network calls of any kind — passwords are generated and stay on your machine.
- 🗂️ No logs, history files, or caches — nothing touches disk unless you explicitly save it.
- 🔍 Fully open source, so you (or anyone) can audit exactly how passwords are generated.

**Entropy reference table** *(approximate, assumes a strong offline brute-force attempt; real-world time depends heavily on the hashing algorithm protecting the password):*

| Length | Character Set | Entropy | Approx. Brute-Force Time |
|:---:|---|:---:|---|
| 8 | letters + digits | ~47 bits | minutes to hours |
| 12 | letters + digits + symbols | ~78 bits | centuries |
| 16 | letters + digits + symbols | ~104 bits | effectively uncrackable |
| 20+ | letters + digits + symbols | ~130+ bits | effectively uncrackable |

<br>

## 🧱 Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/secrets-CSPRNG-8B5CF6?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/argparse-CLI-0EA5E9?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/pyperclip-Clipboard-22C55E?style=for-the-badge"/>
</p>

<br>

## 📁 Project Structure

```
SecurePass-Pro/
├── securepass.py          # Main CLI entry point
├── core/
│   ├── generator.py        # Password generation logic
│   ├── strength.py         # Entropy & strength calculator
│   └── clipboard.py        # Clipboard utility
├── requirements.txt
├── README.md
└── LICENSE
```

<br>

## 🤝 Contributing

Contributions are always welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<br>

## 📜 License

<p align="left">
  <img src="https://img.shields.io/badge/License-MIT-F59E0B?style=for-the-badge"/>
</p>

Distributed under the **MIT License**. See [`LICENSE`](./LICENSE) for details.

<br>

<div align="center">

### ⭐ If SecurePass Pro helped you, consider giving it a star!

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0ea5e9,30:7c3aed,70:312e81,100:050816&section=footer&fontColor=ffffff"/>

</div>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=dhruvprajapati6&theme=tokyo-night&hide_border=true&area=true"/>

</div>

---

---

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Cascadia+Code&size=18&pause=1000&color=A78BFA&center=true&vCenter=true&width=550&lines=🔐+Strong+Random+Passwords+Instantly;🎨+Premium+Dark+UI+%2B+Animations;⚡+Zero+Dependencies+—+Pure+Python;📊+Live+Strength+Meter+%2B+Entropy;💾+Copy+%26+Save+in+One+Click" />

<br/><br/>

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Tkinter](https://img.shields.io/badge/Tkinter-GUI-7C3AED?style=for-the-badge&logo=python&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Mac%20%7C%20Linux-10B981?style=for-the-badge&logo=windows&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-F59E0B?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-✅%20Completed-22c55e?style=for-the-badge)
![Stars](https://img.shields.io/github/stars/dhruvprajapati6/Password-Generator?style=for-the-badge&color=facc15&logo=github)

<br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

</div>

---

## 🌌 Overview

<img align="right" width="320" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExcDJkbHVlbXptdm81NTBrcHFteXpzZjNybmh1OHc2NGtucnZsMWRrbiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/f3iwJFOVOwuy7K6FFw/giphy.gif"/>

> **SecurePass Pro** is a **modern desktop Password Generator** built with **Python + Tkinter**.
> 
> It features a stunning **deep-space dark UI**, real-time **password strength analysis**, **entropy calculation**, animated feedback, and one-click copy/save — all with **zero external dependencies**.

<br/>

### 🎯 Why SecurePass Pro?

- 🔒 Cryptographically strong via `random.SystemRandom`
- 🎨 Premium violet-purple neon dark theme
- 📊 Live strength meter with entropy bits display
- ⚡ Instant — no install, no setup, no internet needed
- 🏆 Beautiful enough to show off in your portfolio

<br clear="right"/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## ✨ Features

<div align="center">

| ⚡ Feature | 📝 Description |
|:---:|:---|
| 🔐 **Secure Generation** | Strong random passwords using Python's `random` module |
| 📏 **Custom Length** | Slider control from **4 to 64** characters |
| 🔡 **Charset Control** | Uppercase · Lowercase · Numbers · Symbols — mix & match |
| 🚫 **Exclude Ambiguous** | Removes confusing chars like `0 O l 1 \|` |
| 📊 **Strength Meter** | Color-coded progress bar: 🔴 → 🟡 → 🟢 → 🔵 |
| 🧮 **Entropy Display** | Shows password entropy in bits at the status bar |
| 📋 **Copy to Clipboard** | One-click copy with green flash animation |
| 💾 **Save to File** | Save password securely via file dialog |
| 🎞️ **Animations** | Cyan flash on generate · Title color cycles · Button press effects |
| 🌑 **Premium Dark UI** | Deep-space dark theme with neon glow accents |
| ⚠️ **Input Validation** | Warns if no charset selected |
| ⚡ **Zero Dependencies** | 100% Python stdlib — no pip required |

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 🛠️ Tech Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=python,vscode,git,github&theme=dark" />

<br/><br/>

| 🔧 Tool | 🎯 Purpose |
|:---:|:---|
| `Python 3.x` | Core programming language |
| `Tkinter` | Built-in GUI framework |
| `ttk` (themed widgets) | Styled progressbar & slider |
| `random` + `string` | Password generation logic |
| `math` | Entropy (bits) calculation |
| `tkinter.filedialog` | Save-to-file dialog |

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 📂 Project Structure

```
📦 Password-Generator/
│
├── 📄 main.py            ← Full app — UI + logic + animations
├── 📄 README.md          ← You are here!
└── 📄 requirements.txt   ← Zero external deps (stdlib only)
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 🚀 Getting Started

### ✅ Prerequisites

```
Python 3.8 or higher
Tkinter (included with Python by default)
```

### 📥 Clone & Run

```bash
# 1️⃣  Clone the repository
git clone https://github.com/dhruvprajapati6/Password-Generator.git

# 2️⃣  Enter the project folder
cd Password-Generator

# 3️⃣  Launch the app
python main.py
```

> 💡 **That's it!** No `pip install`, no virtual env — pure Python magic.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 🎮 How to Use

```
┌─────────────────────────────────────────────────┐
│  🔐  SecurePass Pro                             │
├─────────────────────────────────────────────────┤
│                                                 │
│  [ Generated Password Display ]           [⎘]   │
│                                                 │
│  Strength: ████████████░░░░  Strong 🟢          │
│                                                 │
│  Length ──────●────────── 16                    │
│                                                 │
│  ☑ Uppercase  ☑ Lowercase                      │
│  ☑ Numbers    ☑ Symbols                        │
│  ☐ Exclude ambiguous chars                      │
│                                                 │
│  [ ✨ Generate ]  [ 💾 Save ]  [ 🗑 Clear ]     │
│                                                 │
└─────────────────────────────────────────────────┘
```

| Step | Action |
|:---:|:---|
| **1️⃣** | Set your desired length using the **slider** |
| **2️⃣** | Check/uncheck the **character types** you want |
| **3️⃣** | Hit **✨ Generate Password** — watch it flash! |
| **4️⃣** | See the **strength meter** and **entropy** update live |
| **5️⃣** | Click **⎘** to copy, or **💾 Save** to export |

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 📊 Password Strength Guide

<div align="center">

| 📏 Length | 🔡 Character Set | 💪 Strength | ⏳ Crack Time | 🎯 Use Case |
|:---:|:---:|:---:|:---:|:---|
| ≤ 7 | Any | 🔴 **Weak** | < 1 second | Never use! |
| 8–11 | Lower + Upper | 🟡 **Moderate** | Minutes–Hours | Low-risk only |
| 12–15 | + Numbers | 🟢 **Strong** | Years | Good for most |
| 16–19 | All Types | 🟢 **Very Strong** | Centuries | Recommended |
| 20+ | All Types | 🔵 **Ultra** | Heat death of universe | Maximum security |

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 🗺️ Roadmap

```
✅ Core password generation
✅ Premium dark theme UI
✅ Live strength meter
✅ Entropy calculation
✅ Copy to clipboard
✅ Save to file
✅ Exclude ambiguous chars
✅ Animated flash feedback
🔲 Password history log
🔲 Bulk password generation
🔲 Custom charset input
🔲 Web version (Streamlit)
🔲 Passphrase generator mode
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 📜 License

<div align="center">

Distributed under the **MIT License** — free to use, fork, modify, and share.

```
MIT License © 2025 Dhruv Prajapati
Permission is granted to use this software freely.
```

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

## 📬 Contact & Connect

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-dhruvprajapati6-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/dhruvprajapati6)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Dhruv%20Prajapati-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dhruv-prajapati-616b89362/)
[![Gmail](https://img.shields.io/badge/Gmail-dhruvpprajapati2007-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:dhruvpprajapati2007@gmail.com)

<br/>

**💬 Have feedback or ideas? Open an [Issue](https://github.com/dhruvprajapati6/Password-Generator/issues) or start a [Discussion](https://github.com/dhruvprajapati6/Password-Generator/discussions)!**

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

---

<div align="center">

### 🌟 Show Some Love!

**If this project helped you, please give it a ⭐ — it means a lot!**

<img src="https://media.giphy.com/media/jpVnC65DmYeyRL4LHS/giphy.gif" width="20%"/>

<br/>

```
  ____                            ____
 / ___|  ___  ___ _   _ _ __ ___|  _ \ __ _ ___ ___
 \___ \ / _ \/ __| | | | '__/ _ \ |_) / _` / __/ __|
  ___) |  __/ (__| |_| | | |  __/  __/ (_| \__ \__ \
 |____/ \___|\___|\__,_|_|  \___|_|   \__,_|___/___/

              🔐  Pro  —  Stay Secure!
```

<img src="https://capsule-render.vercel.app/api?type=waving&height=130&color=0:0d0d1a,50:302b63,100:7c3aed&section=footer&animation=fadeIn" />

</div>
