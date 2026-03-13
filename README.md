# CMOS Inverter Design and Analysis for Different Sizing Ratios (KR)

## Overview
This project analyzes the effect of transistor sizing ratio (KR) on the performance of a CMOS inverter. The study focuses on how KR affects switching threshold, noise margins, and propagation delay.

Three CMOS inverter configurations were designed and simulated using **Cadence Virtuoso** with different KR values:

- KR = 0.5
- KR = 1
- KR = 2

The objective is to determine the optimal sizing ratio for balanced switching behavior and maximum noise immunity.

---

## Tools Used

- Cadence Virtuoso
- ADE L simulation environment
- 180 nm CMOS technology
- Supply Voltage: 1.8 V

---

## Design Parameters

| Parameter | Value |
|----------|------|
| Technology | 180 nm |
| VDD | 1.8 V |
| NMOS Width | 850 nm |
| NMOS Length | 180 nm |

PMOS widths were adjusted to achieve different KR values.

---

## CMOS Inverter Designs

### KR = 1 (Balanced Design)

![KR1](images/inverter_Kr1_schematic.png)

PMOS Width = 3.4 µm

---

### KR = 0.5

![KR05](images/inverter_Kr05_schematic.png)

PMOS Width = 1.7 µm

---

### KR = 2

![KR2](images/inverter_Kr2_schematic.png)

PMOS Width = 6.8 µm

---

## Voltage Transfer Characteristics

VTC curves were obtained through DC sweep simulation.

These were used to extract:

- Switching threshold (Vsth)
- VIL
- VIH
- VOH
- VOL

---

## Results

| Parameter | KR=0.5 | KR=1 | KR=2 |
|-----------|--------|------|------|
| Vsth | 814 mV | 895 mV | 1.023 V |
| VIL | 653 mV | 761 mV | 934 mV |
| VIH | 922 mV | 1.019 V | 1.612 V |
| VOL | 103 mV | 102 mV | 66 mV |
| VOH | 1.707 V | 1.678 V | 1.675 V |
| NML | 550 mV | 658 mV | 867 mV |
| NMH | 784 mV | 658 mV | 62 mV |

---

## Propagation Delay

| Parameter | KR=0.5 | KR=1 | KR=2 |
|----------|--------|------|------|
| tplh | 469 ps | 351 ps | 503 ps |
| tphl | 335 ps | 317 ps | 198 ps |
| tp | 402 ps | 334 ps | 350 ps |

---

## Key Observations

- **KR = 1 provides the most balanced design**
- Switching threshold occurs close to **VDD/2**
- **Noise margins are symmetric**
- Propagation delay is minimized

KR values deviating from 1 cause imbalance in noise margins and switching behavior.

---

## Conclusion

For reliable and robust CMOS inverter design, the transistor sizing ratio should be adjusted so that:

KR = 1

This ensures:

- Balanced switching threshold
- Symmetric noise margins
- Minimum propagation delay

---

## Author

Manash Jyoti Barman  
B.Tech Electronics and Communication Engineering  
Tezpur University
