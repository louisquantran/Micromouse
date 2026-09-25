# Micromouse

PCB design for a Micromouse: a small autonomous robot that maps and solves a maze.

The board is designed in [KiCad](https://www.kicad.org/) and built around an STM32F205 microcontroller, with two DC motors with encoders driven by an L293DD H-bridge and IR emitter/phototransistor pairs for wall sensing.

## Repository layout

```
Micromouse/
├── mouse/                        # Main robot board
│   ├── Micromouse_Mainboard/     # Full schematic + PCB (open this one)
│   ├── IR_Emitter+IR_Receiver/   # IR sensing sub-circuit
│   └── Power_Delivery+H_Bridge/  # Power + motor driver sub-circuit
└── rat/                          # Individual sub-circuit projects
    ├── IR_Emitter/
    ├── IR_Receiver/
    ├── Motor_Control(H-Bridge)/
    └── Power_Delivery/
```

## Hardware

| Function | Part |
|---|---|
| Microcontroller | STM32F205RGT6 |
| Motor driver | L293DD dual H-bridge |
| 3.3 V regulator | AZ1117IH-3.3 |
| IR emitters | INL-5AMIR15, switched by BS170 N-MOSFETs |
| IR receivers | SFH 313 FA-3/4 phototransistors |
| Power switch | EG1218 slide switch |
| Motor / battery connectors | JST PH (B2B-PH-K-S) |
| Passives | 0805 resistors and capacitors |
