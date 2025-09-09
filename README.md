ENGLISH >>>

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

-------------------------------------------------------------------------------------

TÜRKÇE >>> 

# UAV Power Distribution Board (PDB)

Çok kademeli güç dağıtım kartı prototipi. Girişte sigorta + TVS + EMI filtresi, ortada **TPS43060 tabanlı boost** ile **sabit bir ara gerilim (~30 V)**, çıkışta ise **4× XL4016 buck kanalı** bulunur. Bu sayede değişken giriş (örn. batarya) koşullarında sabit ve ayarlanabilir çıkışlar elde etmek hedeflenmiştir.  

⚠️ **Not:** Bu kart henüz tam olarak test edilmemiştir. Şematik tasarım ve PCB üretim dosyaları oluşturulmuş, ancak laboratuvar doğrulama ve uzun süreli yük testleri yapılmamıştır.  

## ✨ Özellikler
- **Giriş koruması:** XT30 konnektör, sigorta, 1.5KE27A TVS.  
- **EMI filtresi:** MLCC kapasitör bankı + 22 µH bobin.  
- **Akım ölçümü:** 2×10 mΩ şönt (≈5 mΩ efektif) + ISNS± Kelvin hatları.  
- **Boost aşaması:** TPS43060 (UVLO, soft-start, kompanzasyon ağı ile).  
- **Ara hat:** Geri besleme oranı ≈ 30 V.  
- **Buck kanalları (×4):** XL4016 + Schottky diyot + 47 µH indüktör.  
- **Üretim dosyaları:** Gerber ZIP, BOM.csv, Pick&Place.csv mevcut.  

## 📁 Dizin Yapısı
```
hardware/     → Altium PCB (.pcbdoc), DXF, JSON/SVG
production/   → Gerber ZIP, BOM.csv, PickAndPlace.csv
docs/         → Görseller ve PDF dökümanlar
```

## 🔧 Mevcut Durum
- ✔️ Şematik ve PCB tasarımı tamamlandı.  
- ✔️ Üretim dosyaları (Gerber, BOM, Pick&Place) hazır.  
- ❌ Devre kartı üretildi ancak **henüz kapsamlı test edilmedi**.  
- ❌ Yük altında kararlılık, ripple, EMI ve termal performans doğrulanmadı.  

## 📌 Sonraki Adımlar
- [ ] İlk fonksiyonel test (boost + buck çıkış gerilimleri ölçümü).  
- [ ] Yük altında verimlilik ve sıcaklık ölçümleri.  
- [ ] EMI ve osiloskop ile ripple analizi.  
- [ ] Gerekirse snubber/ferrit boncuk optimizasyonu.  

## 📄 Lisans
MIT Lisansı (özgür kullanım, ticari/kişisel uyarlamaya açık; sorumluluk kullanıcıya aittir).  
