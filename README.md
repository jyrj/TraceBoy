# Trace Boy
Game Boy Emulator Instrumentation

Instrument the mGBA Game Boy emulator to log CPU instructions, memory accesses, and hardware events for testing and analysis.

---
Check the pre-readings here: [Zero week Pre-readings](./docs/pre-reading-sip.md)

## 🚀 Quick Start

1. **Clone & init submodule**  
   ```bash
   git clone https://github.com:jyrj/TraceBoy.git
   cd TraceBoy
   git submodule update --init --recursive


2. **Build mGBA**

   ```bash
   cd emulator
   mkdir build && cd build
   cmake ..            # or `cmake -G "Visual Studio 16 2019" ..` on Windows
   make                # or open the generated solution/project
   cd ../../
   ```

3. **Install Python deps**

   ```bash
   python3 -m venv venv
   source venv/bin/activate     # Windows: venv\Scripts\activate
   pip install --upgrade pip
   pip install -r requirements.txt  # if provided
   ```

---

## 🗂️ Repository Layout - Under development


<!-- /
├── emulator/               # mGBA source (submodule)
├── instrumentation/
│   ├── cpu_logger/         # CPU-trace stubs
│   ├── io_logger/          # I/O-trace stubs
│   └── event_logger/       # (Optional) hardware-event hooks
├── scripts/
│   ├── run_tests.py        # Launch emulator with logging enabled
│   └── analyze_logs.py     # Parse logs & generate metrics
├── roms/
│   └── test_roms/          # Blargg’s & sample game ROMs
├── docs/
│   ├── zero-week-readings.md
│   └── setup_instructions.md
└── README.md -->


---

## ⚙️ Usage - Under development

<!-- ### 1. Instrument & Run

```bash
# e.g. CPU-trace test ROM
python3 scripts/run_tests.py \
  --emulator ./emulator/build/mgba \
  --rom roms/test_roms/cpu_instr.gb \
  --log logs/cpu_trace.log
```

### 2. Analyze Results

```bash
python3 scripts/analyze_logs.py \
  --input logs/cpu_trace.log \
  --output reports/cpu_stats.csv
``` -->

---

## 📚 Documentation

* **docs/sip-pre-readings.md** — 1-hour pre-readings
<!-- * **docs/setup\_instructions.md** — detailed install & build steps -->

---

## 🙌 Contributing

1. Fork the repo
2. Add your code under `instrumentation/` or update `scripts/`
3. Commit, push, and open a PR

---

*Happy hacking! 🚀*





