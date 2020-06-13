Sonopi DAC
===
![project phase](https://img.shields.io/badge/project%20phase-Done-blue.svg)

<p align="center">
<img alt="board image" src="https://raw.githubusercontent.com/wiki/opiopan/sonopi-dac/images/sonopi-dac-configuration.jpg" width=800>
</p>

Sonopi DAC is a hat card for Raspberry Pi to add a audio line output capability.
This hat board is designed to adapt to both of formfactor, Raspbery pi model B+ and Raspberry pi Zero.<br>
[TI PCM5122](http://www.ti.com/product/PCM5122?keyMatch=PCM5122&tisearch=Search-EN-everything&usecase=part-number) is isntalled as DAC module, and Sonopi DAC design is compatible with [Hifiberry DAC+ Pro](https://www.hifiberry.com/shop/boards/hifiberry-dac-pro/) from Raspberry Pi point of view. It means that no special driver is necessary to use Sonopi DAC.

This hardware design is published under open source lincence. You can use and modify this design freely. There is also no limitation in commercial use.

## Project Status
Circuit schema design was done. Now I'm working on board art work.<br>
And I'm also considering which production is more feasible for some parts.

## How to setup
Due to enable drivers for Sonopi DAC in Linux ALSA system, add a following line in ```/boot/config.txt```. Then rebooot a Raspberry Pi.

```
dtoverlay=hifiberry-dacplus
```

## PCB Design
<p align="center">
<img alt="PCB schema" src="imagesrc/schema.svg" width=800>
</p>

<p align="center">
<img alt="board image" src="https://raw.githubusercontent.com/wiki/opiopan/sonopi-dac/images/board-top.png" width=800>
</p>

<p align="center">
<img alt="board image" src="https://raw.githubusercontent.com/wiki/opiopan/sonopi-dac/images/board-bottom.png" width=800>
</p>

<p align="center">
<img alt="board image" src="https://raw.githubusercontent.com/wiki/opiopan/sonopi-dac/images/sonopi-dac.jpg" width=800>
</p>

## BOM List
Components               | Value / Product Number      | Remarks
-------------------------|-----------------------------|------------------------------
U1                       | PCM5122                     |
U2                       | MCP1703AT-3302E/CB          | 3.3V LDO
X1                       | 22.5792MHz Oscillator (3225)|
X2                       | 24.576MHz Oscillator (3225) |
R1, R2                   | 470Ω (1608)                 |
C1, C2                   | 1uF (1608)                  |
C3, C5, C7, C11          | 10uF/16V (3216)             |
C4, C6, C8, C12, C13, C14| 0.1uF/100V (1608)           |
C9, C10                  | 2.2uF/25V (2012)            |
C15, C16                 | 2.2nF/50V (1608)            |
J1                       | HLR-3201VXB-004HG           | RCA Jack (White)
J2                       | HLR-3201VXB-003HG           | RCA Jack (Red)
