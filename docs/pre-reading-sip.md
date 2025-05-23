# Instrumenting & Testing a Game Boy Emulator
## Zero-Week Pre-Reading & Setup Guide

*(Target time: Around 1 hour, but tool installation in Part 4 may vary. Please complete before **June 16, 2025**.)*

---

### 1. Welcome & Why This Pre-Work? 

Hi future emulator experts! We're excited for you to join us. This guide helps you set up essential tools and grasp key concepts before we start. By doing this, you'll:

* Understand the Game Boy's basic hardware and emulator structure.
* Install mGBA (our main emulator) and your core development software.
* Be ready to dive into coding and experiments from Day 1!

Don't worry if some things are new—we'll explore everything more deeply together!

---

### 2. Understanding the Game Boy & Emulators 


| # | Link & What to Skim                                                                                                                                                              | Your Key Take-Away                                                                                                |
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| 1 | **Pan Docs - Foreword & Memory Map** <br> [https://gbdev.io/pandocs/](https://gbdev.io/pandocs/) <br> → Skim "Foreword" <br>→ Briefly look at "Memory Map" (focus on ROM, RAM, I/O areas). | The Game Boy has distinct memory sections for different tasks. Pan Docs is the GB technical guide.                |
| 2 | **"Writing a Game Boy Emulator (Cinoop)"** by C. Turt <br> [https://cturt.github.io/cinoop.html](https://cturt.github.io/cinoop.html) <br>→ Read Sections 1-3 (Why, The CPU, Memory). | Get a basic idea of an emulator's main loop (fetch-decode-execute) and how it handles CPU and memory operations. |

---

### 3. Install & Test mGBA - Our Target Emulator! 
This is the Game Boy emulator we'll be working with.

1.  **Download mGBA:**
    * Go to [https://mgba.io/downloads.html](https://mgba.io/downloads.html).
    * Download the latest stable version for your operating system.

2.  **Install mGBA:**
    * **Windows:** Run the downloaded `.exe` installer and follow the prompts. Or, if you downloaded a `.7z/.zip` archive, extract it to a folder (e.g., `C:\mGBA`) and run `mgba.exe` from there.
    * **macOS:** Open the downloaded `.dmg` file. Drag the `mGBA.app` icon into your `Applications` folder.
    * **Linux:**
        * **Option 1 (Recommended): From your distribution's package manager:**
            * Open your Terminal.
            * *Debian/Ubuntu-based:*
                ```bash
                sudo apt update
                sudo apt install mgba-qt
                ```
            * *Fedora-based:*
                ```bash
                sudo dnf install mgba-qt
                ```
        * **Option 2: From the mGBA website:** Download an AppImage or other Linux package. For an AppImage, make it executable (`chmod +x file.AppImage`) and run it (`./file.AppImage`).

3.  **Test mGBA:**
    * Find a public domain Game Boy ROM. Search "Game Boy public domain ROMs" (e.g., on PDRoms or Archive.org for "Tetris (World) Game Boy ROM"). Download a `.gb` file.
    * Open mGBA. Go to `File > Load ROM` and select the `.gb` file.
    * **Goal:** Confirm the game loads and you can see it running. This means mGBA is set up!

---

### 4. Setting Up Your Development Toolkit (...Take your time!)

This part involves installing several tools we'll use daily. Follow carefully. If you get stuck on one, try the next, and we can troubleshoot on Day 1.

**1. Git (Version Control):**
* Go to [https://git-scm.com/downloads](https://git-scm.com/downloads).
* Download and install Git for your OS, accepting default options during installation.
* **Linux:** If not pre-installed, use your package manager:
    * *Debian/Ubuntu-based:* `sudo apt install git`
    * *Fedora-based:* `sudo dnf install git`

**2. Visual Studio Code (VS Code - Code Editor):**
* Go to [https://code.visualstudio.com/download](https://code.visualstudio.com/download).
* Download and install VS Code for your OS.
    * **Linux:** You can often install via your distribution's software center/package manager (search for "code") or download `.deb`/`.rpm` packages from the website.
* **Install C/C++ Extension:** Open VS Code. Go to the Extensions view (click the square icon on the left sidebar or Ctrl+Shift+X). Search for "C/C++" by Microsoft. Click Install.

**3. Python (Programming Language):**
* Go to [https://www.python.org/downloads/](https://www.python.org/downloads/) to see the latest stable Python 3.x version.
* **Windows:** Download the installer. **Important:** Check the box that says "**Add Python to PATH**" during installation.
* **macOS:** Download and run the installer. Python might already be installed; this ensures a recent version and `pip`.
* **Linux:** Python 3 is usually pre-installed. Check with `python3 --version`. To ensure `pip` and `venv`:
    * *Debian/Ubuntu-based:*
        ```bash
        sudo apt update
        sudo apt install python3 python3-pip python3-venv
        ```
    * *Fedora-based:*
        ```bash
        sudo dnf install python3 python3-pip
        ```

**4. C/C++ Compiler Toolchain (To build code):**
* **Windows:**
    * We recommend Visual Studio Community Edition with C++ workload.
    * Go to [https://visualstudio.microsoft.com/vs/community/](https://visualstudio.microsoft.com/vs/community/). Download the "Community" installer.
    * Run the installer. On the "Workloads" screen, check "**Desktop development with C++**". Click Install.
* **macOS:**
    * You'll need Xcode Command Line Tools.
    * Open Terminal. Type `xcode-select --install` and press Enter. If prompted, click "Install".
* **Linux:**
    * You'll need GCC (g++) and `make`.
    * Open Terminal.
    * *Debian/Ubuntu-based:*
        ```bash
        sudo apt update
        sudo apt install build-essential
        ```
    * *Fedora-based:*
        ```bash
        sudo dnf groupinstall "Development Tools"
        ```
        (Or: `sudo dnf install gcc-c++ make`)

---

### 5. Hardware & Software Recap

* **Hardware Needed:**
    * Windows 10/11, or a recent macOS, or a common Linux distribution.
    * Modern CPU, at least 8 GB RAM (16 GB better).
    * ~10-20 GB free disk space (VS Community can be large).
    * Internet access.
* **Software You Should Have Attempted to Install:**
    1.  mGBA (Emulator)
    2.  Git (Version Control)
    3.  Visual Studio Code (Code Editor) with C/C++ Extension
    4.  Python 3.x
    5.  C/C++ Compiler Toolchain

---

### 6. What to Bring on Day 1 (June 16, 2025) & Troubleshooting

* Your laptop with the software above installed (or attempted!).
* **Crucially, ensure mGBA opens and runs a Game Boy ROM.**
* Notes/questions from readings or installations.
* **Installation Hurdles?** Don't panic! Software setup can be tricky. If you get stuck on a tool in Part 4, note the error or where you stopped. The most important thing is to have mGBA working (Part 3). We will dedicate time on Day 1 to ensure everyone's environment is fully operational.
* If you have specific issues, email your mentor before June 16 with a screenshot of the problem if possible.

We're looking forward to an amazing summer of coding with you!