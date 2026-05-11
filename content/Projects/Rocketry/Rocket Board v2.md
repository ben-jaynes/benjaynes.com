---
title: Rocket Board V2
date: 2025-09-26
tags:
  - "#rocketry"
  - "#pcb"
draft: true
---

## Introduction

After using the first revision of my model rocket control board in [TARC 2025](/projects/tarc-2025) I decided to create a second version to solve many of the issues and inefficiencies that I ran into with V1. Some of the improvements that I aimed to make include:

- Reduced size
- Onboard storage (no microSD card)
- Faster processor
- Higher resolution barometer data

along with some other small fixes.


## Microcontroller

This board was completely redesigned from the ground up, largely due to using a new microcontroller. Previously I used an SAMD21 but for this version I decided to go with a RP2040 due to its low price, high performance and documentation. 

| | SAMD21 | RP2040 |
| --- | --- | --- |
| Architecture | Dual ARM Cortex-M0+ | ARM Cortex-M0+ |
| Speed | 133MHz | 48 MHz |
| Datasheet | [link](https://pip-assets.raspberrypi.com/categories/814-rp2040/documents/RP-008371-DS-1-rp2040-datasheet.pdf?disposition=inline) | [link](https://ww1.microchip.com/downloads/en/DeviceDoc/SAM-D21DA1-Family-Data-Sheet-DS40001882G.pdf) | 

## Storage

One part of the original design that I wanted to change was the use of a microSD card for storing flight data. Although it was easy to implement, this solution was large, prone to mechanical failure during flight and annoying to gather data with. After learning how to expose an onboard flash chip as a USB mass storage device (essentially a flash drive), I decided to use a secondary flash chip to store the flight logs. The RP2040 already requires one for program storage so my new board has two flash chips.
