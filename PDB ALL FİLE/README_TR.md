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
