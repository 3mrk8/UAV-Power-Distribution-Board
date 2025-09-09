# UAV Power Distribution Board (PDB)

A multi-stage power distribution board prototype. At the input, it features a fuse + TVS + EMI filter; in the middle, a **TPS43060-based boost converter** provides a **stable intermediate rail (~30 V)**; and at the output, there are **4× XL4016 buck channels**. This design aims to deliver stable and adjustable outputs even under variable input conditions (e.g., battery sources).  

⚠️ **Note:** This board has not been fully tested yet. The schematic and PCB production files have been prepared, but laboratory validation and long-term load testing have not been performed.  

## ✨ Features
- **Input protection:** XT30 connector, fuse, 1.5KE27A TVS.  
- **EMI filter:** MLCC capacitor bank + 22 µH inductor.  
- **Current sensing:** 2×10 mΩ shunts (≈5 mΩ effective) + ISNS± Kelvin sense lines.  
- **Boost stage:** TPS43060 (with UVLO, soft-start, and compensation network).  
- **Intermediate rail:** Feedback ratio set to ≈ 30 V.  
- **Buck channels (×4):** XL4016 + Schottky diode + 47 µH inductor.  
- **Production files:** Gerber ZIP, BOM.csv, Pick&Place.csv included.  

## 📁 Directory Structure
```
hardware/     → Altium PCB (.pcbdoc), DXF, JSON/SVG
production/   → Gerber ZIP, BOM.csv, Pick&Place.csv
docs/         → Images and PDF documentation
```

## 🔧 Current Status
- ✔️ Schematic and PCB design completed.  
- ✔️ Production files (Gerber, BOM, Pick&Place) ready.  
- ❌ PCB manufactured but **not fully tested yet**.  
- ❌ Stability, ripple, EMI, and thermal performance under load not verified.  

## 📌 Next Steps
- [ ] Initial functional test (measure boost + buck output voltages).  
- [ ] Efficiency and thermal measurements under load.  
- [ ] EMI and ripple analysis with oscilloscope.  
- [ ] Add snubber/ferrite bead optimization if needed.  

## 📄 License
MIT License (free for personal/commercial use; responsibility remains with the user).  
