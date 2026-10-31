# Using the Solar MeshCore Repeater

This rooftop unit runs **MeshCore Repeater** firmware. After setup it mostly runs unattended: companion radios on the same mesh use it automatically for range.

## What you need

- LilyGo T-Beam 915 MHz (revision + LoRa chip identified)
- Antenna attached **before any transmit**
- Power via **USB/5V** only for this solar design (18650 empty; do **not** wire LiFePO4 to B+/B−)
- Chrome or Edge (Web Serial) for flash/config
- A companion MeshCore node/app on the same radio preset to verify adverts

## 1. Flash Repeater firmware

1. Connect the T-Beam by USB (antenna fitted).
2. Open [flasher.meshcore.io](https://flasher.meshcore.io).
3. Select the **exact** board (v1.1 AXP192 vs v1.2/Supreme AXP2101; SX1262 vs SX1276).
4. Choose role **Repeater** → Flash. Do not disconnect until finished.

## 2. Configure

Open **Repeater Setup** on the flasher, or use [config.meshcore.io](https://config.meshcore.io). Enable advanced settings if needed.

| Setting | Guidance |
|---------|----------|
| Name | Clear label, e.g. `Callsign_Roof_R1` |
| Admin password | Change from default; store securely |
| Radio | Match your local mesh — US/CA often **910.525 MHz / 62.5 kHz / SF7 / CR5** (confirm with your group) |
| Advert interval | **60** minutes |
| Flood advert interval | **24** hours (do not set aggressively) |
| Flood max | **64** (or community default) |
| Path hash mode | Often **3-byte (2)** if that is your region default |
| GPS | **Off** for fixed rooftop |
| Location | Optional; use coarse coords if privacy matters |
| Clock | **Sync after every reboot** |

Save → reboot → reconnect → sync clock → **Send advert**. A nearby companion should receive it.

## 3. Bench-test before install

1. Confirm settings survive a reboot.
2. Confirm remote admin from your companion while USB is still easy.
3. Run ≥**72 h** on the battery stack with the panel covered (or equivalent runtime check).
4. Keep USB recovery practical until the rooftop install is verified.

## 4. Day-to-day use

- **Companions** (phones / handheld MeshCore nodes) on the **same radio preset** use the mesh normally. The repeater extends range when it is in the path — no daily login required.
- **Admin** (password): rename, change radio/advert settings, force an advert, check status — via USB setup tools or remote admin from a companion.
- After any power cycle, **resync the clock** so adverts are not treated as stale.

## 5. Site install (power + mounts)

**Power order:** battery → controller → panel last. Fuse battery **+** near the pack. Feed T-Beam on USB/5V only.

**Mounting diagrams**

| Topic | Diagram |
|-------|---------|
| Parts inside the box | `meshcore-tbeam-enclosure-layout.jpg` |
| Enclosure on wall/eave or mast | `meshcore-tbeam-enclosure-site-mount.jpg` |
| Solar panel Z-brackets or mast | `meshcore-tbeam-solar-panel-mount.jpg` |
| Wiring | `meshcore-tbeam-wiring-diagram.jpg` |

Hardware lists: [BOM.md](BOM.md) (outdoor mounts #11) · [BOM-enclosure-mounting.md](BOM-enclosure-mounting.md) (inside-box fasteners).

## Troubleshooting

| Symptom | Check |
|---------|--------|
| Won’t flash / won’t radio | Wrong board/radio/PMIC variant in flasher |
| No TX / weak signal | Antenna missing or wrong connector path |
| Nobody hears you | Radio preset doesn’t match local mesh |
| Adverts ignored after reboot | Clock not synced |
| Mesh congested / complaints | Flood advert interval too short |

## Official links

| Resource | URL |
|----------|-----|
| Web flasher | https://flasher.meshcore.io |
| Repeater / room config | https://config.meshcore.io |
| Flash & configure walkthrough | https://meshcore.ca/meshcore/flash-repeater/ |
| T-Beam build notes | https://wiki.meshamerica.com/books/diy-build-guides/page/t-beam-build-guide-ttgolilygo |
