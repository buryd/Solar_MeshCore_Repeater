# Solar MeshCore Repeater

Solar-powered **MeshCore** rooftop bridge repeater design for **US/CA (902–928 MHz)**, built around a **LilyGo T-Beam**.

| Spec | Value |
|------|--------|
| Role | Rooftop bridge |
| Autonomy | 3–5+ days |
| Access | Serviceable rooftop |
| Radio | LilyGo T-Beam 915 MHz |
| Firmware | MeshCore **Repeater** |

## Architecture

![Architecture](meshcore-tbeam-rooftop-architecture.jpg)

**Power path:** Solar panel → LiFePO4 charge controller → LiFePO4 battery → 5 V regulator → T-Beam USB/5V  

Do **not** connect LiFePO4 to the T-Beam `B+`/`B−` pads — the onboard AXP charger targets ~4.2 V (Li-ion) and can overcharge LFP.

## Wiring

![Wiring diagram](meshcore-tbeam-wiring-diagram.jpg)

Terminal order: connect **battery first**, then panel. Fuse battery **+** near the pack. Feed the T-Beam only on **USB/5V**; leave the 18650 holder empty. RF: outdoor N-male omni → N-female–to–SMA pigtail → T-Beam LoRa SMA.

## Bill of materials

See [BOM.md](BOM.md) for a priced parts list. Full build including LilyGo T-Beam is ~**$236** (~**$240–280** with tax/shipping; Oct 2026 retail estimates). If the T-Beam is already on hand, remaining parts are ~**$190**. Inside-box fasteners (standoffs, VHB, battery strap, etc.) are in [BOM-enclosure-mounting.md](BOM-enclosure-mounting.md) (~**$57**).

## How to use

Full flash, configure, bench-test, and day-to-day steps: **[USAGE.md](USAGE.md)**.

1. Identify T-Beam revision (v1.1 AXP192 vs v1.2/Supreme AXP2101) and LoRa chip (SX1262 vs SX1276).
2. Flash **Repeater** firmware: [flasher.meshcore.io](https://flasher.meshcore.io)
3. Configure radio to match your local mesh (US/CA often `910.525,62.5,7,5` — confirm with your group).
4. Disable GPS for fixed rooftop use; keep flood advert interval long.
5. Bench-test ≥72 h with the panel covered before install.

## Mounting

**Enclosure (site)** — under eave/wall preferred, or mast/pole. Glands face down. Panel and antenna stay outside.

![Enclosure site mounting](meshcore-tbeam-enclosure-site-mount.jpg)

**Solar panel** — Z-brackets on roof/wall, or U-bolts on a mast (keep antenna clear).

![Solar panel mounting](meshcore-tbeam-solar-panel-mount.jpg)

Inside-box layout: `meshcore-tbeam-enclosure-layout.jpg`. Fasteners: [BOM-enclosure-mounting.md](BOM-enclosure-mounting.md).

## Safety

- Fuse the battery positive lead close to the pack.
- Attach the antenna before any transmit.
- Use a charge controller with **0 °C charge cutoff** in freezing climates.
- Seal outdoor RF and cable entries; mount glands facing down.

## License

Documentation and diagrams in this repository are provided as-is for community reuse. Hardware trademarks (LilyGo, etc.) belong to their owners.
