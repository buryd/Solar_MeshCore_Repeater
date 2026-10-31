# BOM — Enclosure mounting (internals)

**Purpose:** Fix T-Beam, charge controller, 5 V supply, and LiFePO4 pack inside the IP65/IP67 box so nothing rattles or shorts.  
**Prices:** approx. USD retail (Oct 2026). Tax/shipping excluded. Verify stock before buy.  
**Assumes:** Main build already covers enclosure (#8), glands (#9), USB bulkhead (#10), outdoor panel mounts (#11), weather kit (#12) in [BOM.md](BOM.md).

**Mount rule:** Fasten parts to the box **backplate / base bosses**, not the lid. Keep the T-Beam on **nylon** standoffs (non-conductive). Glands and USB bulkhead go on the **bottom** wall.

---

## What each part is mounted with

| Component | Mount method | Hardware from this BOM |
|-----------|--------------|------------------------|
| LilyGo T-Beam | M2/M3 nylon standoffs through PCB holes into backplate | M1, M2 |
| PWM charge controller | Screw ears into plate, or VHB + zip-tie backup | M3, M5 (or M4 if ears fit) |
| 12 V→5 V buck / USB brick | VHB / foam tape; zip-tie if no flat face | M3, M5 |
| LiFePO4 pack | Hook-and-loop or battery strap against wall/floor | M6 |
| Inline fuse holder | Zip-tie or adhesive clip near battery + | M5, M7 |
| Cable glands / USB bulkhead | Panel nuts in drilled bottom holes (from main BOM) | tools M8; sealant from weather kit |
| Hookup wire | Adhesive cable clips; slack loops | M7 |

---

## Recommended mounting kit (single enclosure)

| # | Item | Spec / notes | Qty | Unit $ | Ext $ | Source |
|---|------|--------------|-----|--------|-------|--------|
| M1 | **M3 nylon standoff kit** | Male/female spacers + screws + nuts, mixed 6–20 mm. Non-conductive. Use 4× for T-Beam if holes are M3. | 1 | 6.99 | 6.99 | [Amazon M3 nylon standoff kit ~600 pcs](https://www.amazon.com/Nylon-Standoff-Fastener-Kit-Motherboard/dp/B0G3XCGSNV) |
| M2 | **M2 screw / spacer assortment** | Many T-Beam revisions use smaller PCB holes — keep M2×4–8 mm nylon or machine screws + nuts on hand. | 1 | 5.99 | 5.99 | Amazon “M2 nylon screw nut kit” |
| M3 | **3M VHB or outdoor foam tape** | 12–19 mm wide, outdoor-rated. Mounts buck brick / controller without ears; cut pads ~25×25 mm. | 1 | 9.99 | 9.99 | [Amazon 3M VHB / outdoor mounting tape](https://www.amazon.com/s?k=3M+VHB+tape) · hardware store |
| M4 | **#4 / M3 machine screws + nuts (short pack)** | For controller ears or backplate if box bosses need remount. Stainless preferred. | 1 | 4.99 | 4.99 | Hardware store / Amazon stainless assortment |
| M5 | **UV-resistant zip ties** | 4–8 in, black UV. Backup straps for modules + fuse holder; do not rely on alone for heavy battery. | 1 | 5.49 | 5.49 | Hardware / Amazon UV cable ties |
| M6 | **Industrial hook-and-loop or battery strap** | Secure 12.8 V 6 Ah pack flat against enclosure wall/floor. | 1 | 7.99 | 7.99 | Amazon industrial Velcro / “battery strap 20mm” |
| M7 | **Adhesive cable clips / mounts** | Route power and RF pigtail; keep strain off SMA and USB. | 1 | 5.49 | 5.49 | Amazon adhesive cable clips |
| M8 | **Step drill or hole saw set (glands)** | Match PG7/PG9 / USB bulkhead OD. Skip if you already own bits. | 1 | 9.99 | 9.99 | Harbor Freight / Amazon step bit |
| | | | | **Mounting kit** | **56.92** | |

### Totals

| | Amount |
|--|--------|
| **Mounting kit (M1–M8)** | **~$57** |
| Est. tax (example 8%) | ~$5 |
| **All-in mounting estimate** | **~$60–70** |
| If you already own drill bits (skip M8) | **~$47** |
| Consumables only if standoffs/tape/ties already on bench | **~$15–25** |

Kits M1/M2 leave leftover hardware for later nodes.

---

## Already in main BOM (do not double-buy)

| Main BOM # | Item | Mounting role |
|------------|------|----------------|
| 8 | IP65/IP67 enclosure | Backplate / bosses are the mounting surface |
| 9 | Cable glands PG7/PG9 | Bottom-wall penetrations for PV, load, RF |
| 10 | Waterproof USB bulkhead | Panel-nut mount; short pigtail to T-Beam USB |
| 11 | Panel Z-brackets / pole clamps / UV ties | **Outside** box — panel & enclosure to roof/pole |
| 12 | Silicone, self-fusing tape, desiccant | Seal glands; RF weatherproof; humidity control |
| 13 | Hookup wire / connectors | Power runs inside box |

Enclosure + glands + bulkhead + weather kit from the main list ≈ **$43** if buying those lines only for the box itself.

---

## Optional upgrades

| # | Item | Why | Est. $ | Source |
|---|------|-----|--------|--------|
| O1 | **DIN rail + module clips** | Cleaner layout if controller/buck have DIN footprints | +12–20 | Amazon / DigiKey DIN TS35 short length |
| O2 | **3D-printed mounting plate (PETG/ASA)** | Custom cutouts for T-Beam + modules; bolts to factory backplate holes | +0 DIY / +10–25 print | Printables / MakerWorld “junction box mounting plate” |
| O3 | **M3 brass heat-set inserts** | Stronger threads in printed plates | +6 | Amazon heat-set insert kit |
| O4 | **N-female bulkhead connector** | Antenna on box wall instead of gland + flying pigtail | +8–15 | Amazon / Rokland N bulkhead |
| O5 | **Larger enclosure (≥200×150×100 mm)** | Room for battery + standoffs without stacking | +10–20 | Amazon IP65 junction box |

---

## Budget vs recommended vs premium (mounting only)

| Build | Approach | Approx. |
|-------|----------|---------|
| **Budget** | VHB + zip ties + Velcro; hand-drill with existing bits; skip M1 kit if you have 4 nylon standoffs | **~$25–35** |
| **Recommended (this BOM)** | Nylon standoff kits + VHB + Velcro + clips + step bit | **~$57** |
| **Premium** | Printed PETG plate + heat-set inserts + DIN rail + N bulkhead | **~$90–120** |

---

## Install checklist

1. Dry-fit backplate; mark gland / USB holes on **bottom** face.  
2. Drill; install glands and USB bulkhead; snug locknuts (silicone on threads if needed).  
3. Mount T-Beam on nylon standoffs — board clear of walls; **18650 empty**.  
4. Stick or screw controller and 5 V supply; strap battery; fuse on battery **+** near pack.  
5. Clip cables; leave service loops; connect USB bulkhead → T-Beam; RF pigtail → SMA.  
6. Desiccant in, lid gasket seated, outdoor RF joints taped.

---

## Related docs

| Resource | File / URL |
|----------|------------|
| Main parts BOM | [BOM.md](BOM.md) |
| Enclosure layout diagram | `meshcore-tbeam-enclosure-layout.jpg` |
| Wiring diagram | `meshcore-tbeam-wiring-diagram.jpg` |
| Enclosure choice notes | https://wiki.meshamerica.com/books/diy-build-guides/page/choosing-an-enclosure |

*Prices fluctuate; re-check linked listings at purchase time.*
