# BOM — Solar MeshCore Rooftop Bridge (LilyGo T-Beam)

**Role:** US/CA rooftop bridge repeater · **Autonomy:** 3–5 days · **Access:** rooftop-serviceable  
**Prices:** approx. USD retail (Oct 2026). Exclude tax/shipping unless noted. Verify stock before buy.

**Power rule:** Solar → LFP controller → LiFePO4 → 5 V regulator → T-Beam USB/5V.  
Do **not** connect LiFePO4 to T-Beam B+/B− (AXP charges to ~4.2 V).

---

## Recommended build (single unit)

| # | Item | Spec / notes | Qty | Unit $ | Ext $ | Source |
|---|------|--------------|-----|--------|-------|--------|
| 1 | **LilyGo T-Beam 915 MHz** | Match flasher to radio (SX1262/SX1276) + PMIC (v1.1 AXP192 / v1.2 AXP2101). GPS off when deployed. | 1 | 45.99 | **45.99** | [Amazon LilyGo T-Beam](https://www.amazon.com/LILYGO-Meshtastic-Development-CH9102F-Soldered/dp/B0B63FV7FR) |
| 1a | *Alt: T-Beam Supreme 915* | ESP32-S3 + AXP2101; use instead of #1 if preferred | 1 | 52.97 | — | [Rokland T-Beam Supreme](https://store.rokland.com/collections/lilygo-t-beam-series) |
| 2 | **Outdoor LoRa antenna** | 5–5.8 dBi omni, 902–928 MHz, N-male fiberglass | 1 | 14.95 | 14.95 | [SparkFun 5.8 dBi N](https://www.sparkfun.com/lora-fiberglass-antenna-type-n-5-8dbi-902-928mhz.html) |
| 2a | *Alt antenna* | Compact 5 dBi N-male omni | 1 | 14.97 | — | [Rokland ALFA AOA-915-5ACM](https://store.rokland.com/products/alfa-aoa-915-5acm-5-dbi-omni-outdoor-915mhz-802-11ah-mini-antenna-for-lora-halow-application) |
| 3 | **RF pigtail** | N-female → SMA-male (match T-Beam LoRa SMA), ≤1–2 m low-loss | 1 | 10.97 | 10.97 | [Rokland SMA-male to N-female cable](https://store.rokland.com/products/sma-male-to-n-female-6-ft-antenna-extension-coaxial-cable-240-low-loss) · [short adapter pigtail](https://store.rokland.com/products/sma-male-to-n-female-connector-adapter-pigtail) |
| 4 | **Solar panel + PWM controller kit** | 20 W mono + waterproof 10 A PWM (Li-compatible). Prefer LFP setting if available. | 1 | 49.99 | 49.99 | [Amazon Newpowa 20W kit](https://www.amazon.com/Newpowa-Solar-Charging-Controller-Regulator/dp/B00LDISZZA) · [Newpowa direct ~$40.79](https://www.newpowa.com/20w-waterproof-monocrystalline-solar-kit/) |
| 5 | **LiFePO4 battery** | 12.8 V 6 Ah (~76.8 Wh) w/ BMS — exceeds 3–5 day target for T-Beam idle. Includes LFP charger in many listings (use solar controller for rooftop charge). | 1 | 24.99 | **24.99** | [Amazon OCELL 12V 6Ah LFP](https://www.amazon.com/OCELL-6Ah-LiFePO4-Cycle-Battery/dp/B0G8JKL4GJ) |
| 5a | *Alt pack* | Same capacity; search current stock if ASIN rotates | 1 | 23.99 | — | [Amazon 12V 6Ah LiFePO4](https://www.amazon.com/s?k=12V+6Ah+LiFePO4+battery) · [DC HOUSE search](https://www.amazon.com/s?k=DC+HOUSE+12V+6Ah+LiFePO4) |
| 6 | **12 V → 5 V USB supply** | Buck / USB out to power T-Beam USB (skip if using 5a bundle) | 1 | 14.99 | 14.99 | [Amazon DC HOUSE 12V→5V](https://www.amazon.com/DC-HOUSE-Converter-Battery-Chargers/dp/B0DJ2SNQNN) |
| 6a | *Budget alt* | Bare 12 V→5 V buck module (wire to 5V pin) | 1 | 6.00 | — | [Amazon MP1584 mini buck](https://www.amazon.com/MP1584EN-Converter-Adjustable-Compatible-Raspberry/dp/B089GV88DK) |
| 7 | **Inline fuse + holder** | ATC/blade ~3–5 A on battery **+** near pack | 1 | 5.00 | 5.00 | [Amazon ATC inline fuse holders](https://www.amazon.com/Gauge-Inline-Fuse-Holder-Blade/dp/B09F1VQPFC) |
| 8 | **IP65/IP67 enclosure** | ≥150×110×70 mm (fits T-Beam + converter + glands); larger if battery inside | 1 | 18.00 | 18.00 | [Amazon LANUCN IP65 150×110×70 w/ glands](https://www.amazon.com/LANUCN-Waterproof-Rectangular-Junction-Diameter/dp/B09Q2889CY) · [larger IP67 box](https://www.amazon.com/Joisyoya-Electrical-Waterproof-Weatherproof-Electronics/dp/B0D9CWHNR4) |
| 9 | **Cable glands** | PG7/PG9 pack (antenna/power/USB) | 1 | 5.00 | 5.00 | Often included with [#8](https://www.amazon.com/LANUCN-Waterproof-Rectangular-Junction-Diameter/dp/B09Q2889CY); else [Amazon PG7/PG9 gland pack](https://www.amazon.com/s?k=PG7+PG9+cable+gland+pack) |
| 10 | **USB bulkhead / recovery** | Waterproof USB-C or Micro-USB extension for rooftop flash without opening often | 1 | 8.00 | 8.00 | [Amazon waterproof Micro-USB panel mount](https://www.amazon.com/Jenngaoo-Waterproof-Connector-Industrial-Equipment/dp/B0956RG3TN) · [USB-C bulkhead](https://www.amazon.com/QIANRENON-Waterproof-Connector-Feedthrough-Bulkhead/dp/B0D9612YVP) |
| 11 | **Mounting hardware (outdoor)** | Panel Z-brackets or pole clamps, U-bolts, UV zip-ties — **outside** the box | 1 | 15.00 | 15.00 | [Amazon solar Z-brackets](https://www.amazon.com/s?k=solar+panel+Z+brackets) · [pole clamps / U-bolts](https://www.amazon.com/s?k=antenna+pole+mount+U-bolt) · inside-box: [BOM-enclosure-mounting.md](BOM-enclosure-mounting.md) (~$57) |
| 12 | **Weather kit** | Silicone sealant, self-fusing tape (RF joints), silica desiccant pack | 1 | 12.00 | 12.00 | [Amazon outdoor silicone](https://www.amazon.com/s?k=outdoor+silicone+sealant) · [self-fusing silicone tape](https://www.amazon.com/s?k=self+fusing+silicone+tape) · [silica desiccant packs](https://www.amazon.com/s?k=silica+gel+desiccant+packs) |
| 13 | **Hookup wire / connectors** | 16–18 AWG, Anderson/SAE as needed, ring terminals | 1 | 10.00 | 10.00 | [Amazon 16 AWG hookup wire](https://www.amazon.com/s?k=16+AWG+hookup+wire+red+black) · [Anderson Powerpole](https://www.amazon.com/s?k=Anderson+Powerpole+connectors) · [ring terminals](https://www.amazon.com/s?k=ring+terminals+assortment) |
| | | | | **Parts to buy** | **234.88** | |

### Totals (recommended line items 1–13)

| | Amount |
|--|--------|
| **Parts to buy (incl. T-Beam)** | **~$235** |
| Est. tax (example 8%) | ~$19 |
| Est. shipping (if not free) | $0–25 |
| **All-in estimate** | **~$240–280** |
| If T-Beam already owned, subtract #1 | **~$189** parts / ~$195–230 all-in |

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
| Charge controller with **0 °C charge cutoff** / LFP profile | Many kit PWMs lack true cold-charge inhibit | +25–60 | [Victron SmartSolar](https://www.amazon.com/s?k=Victron+SmartSolar+MPPT) · [LFP cold-cutoff controllers](https://www.amazon.com/s?k=LiFePO4+solar+charge+controller+low+temperature) |
| Larger enclosure or battery under-eave | Keep pack warmer; still accessible | +10–20 | [Amazon larger IP67 box](https://www.amazon.com/Joisyoya-Electrical-Waterproof-Weatherproof-Electronics/dp/B0D9CWHNR4) |

If winters go below freezing, treat the cold-cutoff controller as **required**, not optional.

---

## Firmware / software (no hardware cost)

| Resource | URL |
|----------|-----|
| MeshCore flasher | https://flasher.meshcore.io |
| Repeater / room config | https://config.meshcore.dev |
| T-Beam build notes | https://wiki.meshamerica.com/books/diy-build-guides/page/t-beam-build-guide-ttgolilygo |
| Usage (flash / operate) | [USAGE.md](USAGE.md) |
| Architecture diagram | `meshcore-tbeam-rooftop-architecture.jpg` |
| Wiring diagram | `meshcore-tbeam-wiring-diagram.jpg` |
| Enclosure layout (internals) | `meshcore-tbeam-enclosure-layout.jpg` |
| Enclosure site mount | `meshcore-tbeam-enclosure-site-mount.jpg` |
| Solar panel mount | `meshcore-tbeam-solar-panel-mount.jpg` |
| Enclosure mounting BOM | [BOM-enclosure-mounting.md](BOM-enclosure-mounting.md) |

---

## Budget vs premium snapshot

| Build | Key swaps | Approx. to buy |
|-------|-----------|----------------|
| **Budget** | T-Beam + ALFA antenna + Newpowa 20W + OCELL 6Ah + bare buck + basic box | **~$210** |
| **Recommended (this BOM)** | T-Beam + SparkFun fiberglass + USB buck + bulkhead + full weather kit | **~$235** |
| **Premium / cold** | Supreme or 1W radio + Bioenno LFP + Victron-class controller + cold cutoff | **~$350–450** |
| **Skip radio** | If T-Beam already on hand, omit #1 | **−$46** |

---

## Buy checklist (order of purchase)

1. Buy **LilyGo T-Beam 915**; confirm **revision + LoRa chip** before flashing.  
2. Buy antenna + pigtail (gender match N ↔ SMA).  
3. Buy solar/LFP/5 V stack; battery → controller → panel wiring; fuse on battery +.  
4. 5 V only into T-Beam USB/5V — empty onboard 18650 holder for this solar design.  
5. Bench 72h covered-panel runtime before roof install.

*Prices fluctuate; re-check linked listings at purchase time.*
