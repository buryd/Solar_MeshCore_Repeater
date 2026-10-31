# BOM — Solar MeshCore Rooftop Bridge (LilyGo T-Beam)

**Role:** US/CA rooftop bridge repeater · **Autonomy:** 3–5 days · **Access:** rooftop-serviceable  
**Prices:** approx. USD retail (Oct 2026). Exclude tax/shipping unless noted. Verify stock before buy.  
**Owned:** LilyGo T-Beam already on hand — **$0** on this BOM (reference retail ~$46 if replacing).

**Power rule:** Solar → LFP controller → LiFePO4 → 5 V regulator → T-Beam USB/5V.  
Do **not** connect LiFePO4 to T-Beam B+/B− (AXP charges to ~4.2 V).

---

## Recommended build (single unit)

| # | Item | Spec / notes | Qty | Unit $ | Ext $ | Source |
|---|------|--------------|-----|--------|-------|--------|
| 1 | **LilyGo T-Beam 915 MHz** | **Already owned.** Match flasher to radio (SX1262/SX1276) + PMIC (v1.1 AXP192 / v1.2 AXP2101). GPS off when deployed. | 1 | 0.00 | **0.00** | On hand (ref. [Amazon ~$46](https://www.amazon.com/LILYGO-Meshtastic-Development-CH9102F-Soldered/dp/B0B63FV7FR)) |
| 1a | *Alt: T-Beam Supreme 915* | Only if buying a second/replacement board | 1 | 52.97 | — | [Rokland T-Beam Supreme](https://store.rokland.com/collections/lilygo-t-beam-series) |
| 2 | **Outdoor LoRa antenna** | 5–5.8 dBi omni, 902–928 MHz, N-male fiberglass | 1 | 14.95 | 14.95 | [SparkFun 5.8 dBi N](https://www.sparkfun.com/lora-fiberglass-antenna-type-n-5-8dbi-902-928mhz.html) |
| 2a | *Alt antenna* | Compact 5 dBi N-male omni | 1 | 14.97 | — | [Rokland ALFA AOA-915-5ACM](https://store.rokland.com/products/alfa-aoa-915-5acm-5-dbi-omni-outdoor-915mhz-802-11ah-mini-antenna-for-lora-halow-application) |
| 3 | **RF pigtail** | N-female → SMA-male (match T-Beam LoRa SMA), ≤1–2 m low-loss | 1 | 12.00 | 12.00 | Rokland / Amazon “N-female to SMA” LoRa cable |
| 4 | **Solar panel + PWM controller kit** | 20 W mono + waterproof 10 A PWM (Li-compatible). Prefer LFP setting if available. | 1 | 49.99 | 49.99 | [Amazon Newpowa 20W kit](https://www.amazon.com/Newpowa-Solar-Charging-Controller-Regulator/dp/B00LDISZZA) · [Newpowa direct ~$40.79](https://www.newpowa.com/20w-waterproof-monocrystalline-solar-kit/) |
| 5 | **LiFePO4 battery** | 12.8 V 6 Ah (~76.8 Wh) w/ BMS — exceeds 3–5 day target for T-Beam idle | 1 | 17.13 | 17.13 | [Amazon Takki 12V 6Ah LFP](https://www.amazon.com/dp/B0CYPQHG28) |
| 5a | *Alt pack* | Same capacity, better brand/support | 1 | 34.99 | — | [DC HOUSE 6Ah + USB converter bundle](https://www.amazon.com/DC-HOUSE-Converter-Charging-Portable/dp/B0GCCZRH5W) |
| 6 | **12 V → 5 V USB supply** | Buck / USB out to power T-Beam USB (skip if using 5a bundle) | 1 | 14.99 | 14.99 | [Amazon DC HOUSE 12V→5V](https://www.amazon.com/DC-HOUSE-Converter-Battery-Chargers/dp/B0DJ2SNQNN) |
| 6a | *Budget alt* | Bare 12 V→5 V buck module (wire to 5V pin) | 1 | 6.00 | — | Amazon / AliExpress mini buck |
| 7 | **Inline fuse + holder** | ATC/blade ~3–5 A on battery **+** near pack | 1 | 5.00 | 5.00 | Hardware / Amazon fuse kit |
| 8 | **IP65/IP67 enclosure** | ≥150×110×70 mm (fits T-Beam + converter + glands); larger if battery inside | 1 | 18.00 | 18.00 | Amazon outdoor junction box (size up vs tiny 65 mm boxes) |
| 9 | **Cable glands** | PG7/PG9 pack (antenna/power/USB) | 1 | 5.00 | 5.00 | Often included with box; else Amazon gland pack |
| 10 | **USB bulkhead / recovery** | Waterproof USB-C or Micro-USB extension for rooftop flash without opening often | 1 | 8.00 | 8.00 | Amazon waterproof USB panel mount |
| 11 | **Mounting hardware (outdoor)** | Panel Z-brackets or pole clamps, U-bolts, UV zip-ties — **outside** the box | 1 | 15.00 | 15.00 | Hardware store / Amazon solar Z-brackets · **Inside-box mounts:** [BOM-enclosure-mounting.md](BOM-enclosure-mounting.md) (~$57) |
| 12 | **Weather kit** | Silicone sealant, self-fusing tape (RF joints), silica desiccant pack | 1 | 12.00 | 12.00 | Hardware / Amazon |
| 13 | **Hookup wire / connectors** | 16–18 AWG, Anderson/SAE as needed, ring terminals | 1 | 10.00 | 10.00 | Hardware / Amazon |
| | | | | **Parts to buy** | **182.06** | |

### Totals (recommended line items 2–13; T-Beam owned)

| | Amount |
|--|--------|
| T-Beam (owned) | **$0** |
| **Parts to buy** | **~$182** |
| Est. tax (example 8%) | ~$15 |
| Est. shipping (if not free) | $0–25 |
| **All-in estimate (remaining)** | **~$185–220** |
| Full retail if buying T-Beam too | ~$228 parts / ~$230–270 all-in |

---

## Energy check (why 6 Ah / 20 W)

| Parameter | Value |
|-----------|--------|
| Pack energy | 12.8 V × 6 Ah ≈ **77 Wh** |
| T-Beam repeater rough draw | ~2–5 Wh/day (GPS off; measure yours) |
| Autonomy at 4 Wh/day | ~**19 days** theoretical → **well above 3–5 days** with cold/derate margin |
| Panel | 20 W recovers pack on modest sun-hours better than 10 W for northern/cloudy roofs |

Mild southern US can drop to a **10 W** panel (~$15–25) and keep the same battery; leave 20 W if snow/shade risk.

---

## Cold-climate add-on (optional)

| Item | Why | Est. $ | Source |
|------|-----|--------|--------|
| Charge controller with **0 °C charge cutoff** / LFP profile | Many kit PWMs lack true cold-charge inhibit | +25–60 | Victron / specialized LFP solar controllers |
| Larger enclosure or battery under-eave | Keep pack warmer; still accessible | +10–20 | — |

If winters go below freezing, treat the cold-cutoff controller as **required**, not optional.

---

## Firmware / software (no hardware cost)

| Resource | URL |
|----------|-----|
| MeshCore flasher | https://flasher.meshcore.io |
| Repeater / room config | https://config.meshcore.dev |
| T-Beam build notes | https://wiki.meshamerica.com/books/diy-build-guides/page/t-beam-build-guide-ttgolilygo |
| Architecture diagram | `meshcore-tbeam-rooftop-architecture.jpg` |
| Wiring diagram | `meshcore-tbeam-wiring-diagram.jpg` |
| Enclosure layout | `meshcore-tbeam-enclosure-layout.jpg` |
| Enclosure mounting BOM | [BOM-enclosure-mounting.md](BOM-enclosure-mounting.md) |

---

## Budget vs premium snapshot

| Build | Key swaps | Approx. to buy (T-Beam owned) |
|-------|-----------|--------------------------------|
| **Budget** | ALFA antenna + Newpowa 20W + Takki 6Ah + bare buck + basic box | **~$155** |
| **Recommended (this BOM)** | SparkFun fiberglass + USB buck + bulkhead + full weather kit | **~$182** |
| **Premium / cold** | Bioenno LFP + Victron-class controller + cold cutoff | **~$300–400** |
| **If replacing radio** | Add standard T-Beam (~$46) or Supreme (~$53) / 1W (~$63) | **+$46–63** |

---

## Buy checklist (order of purchase)

1. Confirm **owned** T-Beam **revision + LoRa chip** before flashing.  
2. Buy antenna + pigtail (gender match N ↔ SMA).  
3. Buy solar/LFP/5 V stack; battery → controller → panel wiring; fuse on battery +.  
4. 5 V only into T-Beam USB/5V — empty onboard 18650 holder for this solar design.  
5. Bench 72h covered-panel runtime before roof install.

*Prices fluctuate; re-check linked listings at purchase time.*
