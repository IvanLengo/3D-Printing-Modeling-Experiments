# QIDI X-MAX 1

## Slicer
- QIDI Slicer
- OrcaSlicer (preferred)

## Materials Tested
- PLA

## Overview of Typical Settings
- Nozzle size: 0.4 mm
- Layer height: 0.2 mm (`0.12 mm` not extensively tested)
- Bed temperature: 55–65°C
- Printing temperature: 185–200°C
- Typical print speeds: 50–60 mm/s
- Standard nozzle configuration with no enclosure modifications

---

## Printer Information & Hardware

### Extruder

| Front View | Rear View |
|---|---|
| ![Extruder Front](images/extruder_front.jpg) | ![Extruder Back](images/extruder_back.jpg) |

---

### Motor / Hardware Information

![Motor Info](images/motor_info.jpg)

---

### Printer Version Information

![Version Information](images/version_pic.jpg)

---

# Printing Notes & Optimization Findings

## Wall Count

Typical configuration:
- `3 walls` with a `0.4 mm nozzle`
- Approximate wall thickness:
  - `3 × 0.4 mm = 1.2 mm`

### Advantages
- Increased structural strength
- Better durability on functional prints

### Disadvantages
- Higher material consumption
- Longer print times

### Notes
- Larger models generally benefit from thicker walls for improved structural stability.

---

## Wall Printing Order

### Inner Walls First
Recommended for:
- Miniatures
- Organic models
- Better overhang support

### Advantages
- Improved surface smoothness
- Better support for external walls

### Disadvantages
- Reduced X-Y dimensional accuracy

### Possible Compensation
- X-Y contour compensation
- X-Y hole compensation

These settings can help restore dimensional accuracy after switching wall order.

---

### Outer Walls First
Recommended for:
- Dimensionally accurate parts
- Mechanical components

### Advantages
- Better dimensional precision
- Cleaner external geometry

### Disadvantages
- Overhangs may degrade more easily
- Surface quality can become less consistent

---

## Optimize Wall Printing Order

Usually disabled unless:
- print time reduction is prioritized
- minor quality tradeoffs are acceptable

---

## Alternate Extra Wall

Behavior:
- Even-numbered layers print normal wall count
- Odd-numbered layers print an additional wall

### Advantages
- Improved layer bonding
- Slightly increased strength

### Disadvantages
- Increased print time
- Additional material usage

---

## Cooling Recommendations (PLA)

Recommended:
- Reduced cooling on first layer
- Near 100% cooling after initial layers

Strong cooling significantly improves:
- bridging
- overhang performance
- stringing reduction

---

## Inner vs Outer Wall Speeds

### Outer Wall
- Usually kept close to nozzle width and lower speed
- Most visible surface section

### Inner Wall
- Less visually important
- Can be printed slightly faster

### Benefits
- Faster print times
- Better infill bonding
- Reduced visible quality impact

---

## Bridging Improvements

Recommended adjustments for PLA:
- Lower nozzle temperatures (`~200°C` or lower)
- Strong part cooling

Cooling performance has major influence on bridge quality.

---

## Ringing / Ghosting Reduction

Common improvements:
- Reduce outer wall print speed
- Lower outer wall acceleration
- Reduce jerk values (if enabled)
- Lower printing temperature slightly

Ringing appears consistently on the QIDI X-MAX 1 during faster prints.

---

## Infill Patterns

### Line
- Faster
- Simpler
- Good general-purpose option

### Gyroid
- Stronger internal structure
- Better load distribution

### Tradeoff
- Longer print times
- Increased slicer complexity

---

## Gap Fill

### External Only
- Improves outer visual quality

### Everywhere
- Improves structural consistency
- Can strengthen weak areas

### Notes
- Aggressive gap fill may negatively affect bridging tests.

---

## Stringing (Major Issue on QIDI X-MAX 1)

Most effective improvements:
- Lower nozzle temperature
- Retraction speed tuning (`40–60 mm/s`)
- Retraction length tuning (`2.0–3.0 mm`)

Stringing remains one of the most common issues on this printer.

---

## Reduce Infill Retraction

### Effect
- Disables excessive Z-hop behavior during infill travel

### Possible Advantages
- Faster print times
- Reduced unnecessary movement

### Possible Disadvantages
- Increased collision risk on poor-quality prints

---


## Firmware / Support Notes

The QIDI X-MAX I is an older printer model, but firmware updates and support resources are still available from QIDI support.

### Support Contacts
- `linda@qd3dprinter.com`
- `sophia@qd3dprinter.com`

### Warranty / After-Sales Support Requirements
Valid proof of purchase may be required, including:
- Order number from QIDI or authorized reseller
- Sales invoice
- Dated sales receipt
- Other valid proof of purchase documentation

---

## Notes

- Individual print folders contain their own dedicated `README.md` files documenting:
  - print settings
  - calibration adjustments
  - observed defects/issues
  - print quality findings
  - images and final results

- Main focus areas include:
  - print optimization
  - dimensional accuracy
  - overhang performance
  - ringing reduction
  - slicer experimentation
