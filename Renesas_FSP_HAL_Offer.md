# Renesas FSP-based Embedded Software

> [!IMPORTANT]
> Unlike a modular multi-repository model, the Renesas RA software offer is delivered through a **monorepo model**: the Flexible Software Package (FSP) HAL drivers, Board Support Packages (BSP), CMSIS device headers, and most middleware are all maintained inside a single repository, [`renesas/fsp`](https://github.com/renesas/fsp). The tables below link directly to the relevant folder inside that repository, or to the dedicated repository where one exists (examples, RX/RZ packages, middleware, AI).

## Table of contents

- [Renesas FSP MCU Packages](#renesas-fsp-mcu-packages)
- [Renesas Application Projects and Examples](#renesas-application-projects-and-examples)
- [Renesas CMSIS](#renesas-cmsis)
- [Renesas FSP HAL Drivers](#renesas-fsp-hal-drivers)
- [Renesas BSP Board Support](#renesas-bsp-board-support)
- [Renesas MW Libraries and Applications](#renesas-mw-libraries-and-applications)
- [Renesas AI and Model Deployment](#renesas-ai-and-model-deployment)
- [Renesas Utilities and miscellaneous](#renesas-utilities-and-miscellaneous)

## Renesas FSP MCU Packages

The Renesas MCU embedded software offer is delivered per product family. The RA family uses the Flexible Software Package (FSP); the RX family uses the RX Driver Package; wireless RA MCUs use the RA Wireless FSP (RAFW).

| MCU package | Description | Repository |
| :--- | :--- | :--- |
| FSP (RA Family) | Production-ready HAL drivers, BSP, RTOS integration and middleware for all RA MCUs | [Go to repository](https://github.com/renesas/fsp) |
| RA Wireless FSP (RAFW) | FSP for Renesas RA Wireless MCUs (e.g., RA4W1) | [Go to repository](https://github.com/renesas/rafw-fsp) |
| RX Driver Package | Official device driver package for the Renesas RX Family (referenced by Smart Configurator) | [Go to repository](https://github.com/renesas/rx-driver-package) |
| IoT Reference (RX) | FreeRTOS + AWS IoT reference integration for RX MCUs | [Go to repository](https://github.com/renesas/iot-reference-rx) |
| RZ FSP (RZ MPU Family) | FSP for the Renesas RZ series (RZ/A, RZ/G, RZ/N, RZ/T, RZ/V) | [Go to repository](https://github.com/renesas/rz-fsp) |

## Renesas Application Projects and Examples

Example projects demonstrate the basic usage of FSP modules on RA boards. Application projects illustrate solutions in various core technologies and map to Renesas Application Notes.

| Package | Description | Repository |
| :--- | :--- | :--- |
| RA FSP Examples | Example projects and application projects for the RA MCU family (per-kit, per-module) | [Go to repository](https://github.com/renesas/ra-fsp-examples) |
| RAFW FSP Examples | Example projects for RA Wireless MCUs | [Go to repository](https://github.com/renesas/rafw-fsp-examples) |
| RZ FSP Examples | Example projects for the RZ MPU family | [Go to repository](https://github.com/renesas/rz-fsp-examples) |
| CPK Examples | Sample code for China Promotion Kits (CPK boards) | [Go to repository](https://github.com/renesas/cpk_examples) |

## Renesas CMSIS

The CMSIS interfaces offer access to the Arm Cortex®-M processor core features and device-specific peripherals of Renesas RA microcontrollers. CMSIS core and device headers are delivered inside the FSP BSP; CMSIS software event/IO tooling is maintained in a dedicated repository.

| CMSIS component | Description | Repository |
| :--- | :--- | :--- |
| FSP BSP (CMSIS core + device) | CMSIS-Core integration and RA device headers, delivered within the FSP BSP | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/bsp) |
| CMSIS-View | CMSIS software pack for software event generation and I/O handling | [Go to repository](https://github.com/renesas/CMSIS-View) |

## Renesas FSP HAL Drivers

The HAL Drivers propose the HAL and register-level driver modules controlling all the hardware peripherals embedded in the Renesas RA products. Each peripheral driver is maintained as a module folder (`r_<peripheral>`) inside the FSP repository. Their usage is illustrated through examples in the [ra-fsp-examples](https://github.com/renesas/ra-fsp-examples) repository.

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| ADC (12/14-bit) | r_adc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_adc) |
| ADC (scalable, _b) | r_adc_b | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_adc_b) |
| DAC | r_dac | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dac) |
| Comparator (High-speed) | r_acmphs | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_acmphs) |
| Comparator (Low-power) | r_acmplp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_acmplp) |
| General PWM Timer | r_gpt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_gpt) |
| Three-Phase PWM | r_gpt_three_phase | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_gpt_three_phase) |
| Asynchronous General-Purpose Timer | r_agt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_agt) |
| SCI UART | r_sci_uart | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_uart) |
| SPI | r_spi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_spi) |
| I2C Master (IIC) | r_iic_master | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iic_master) |
| I2C Slave (IIC) | r_iic_slave | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iic_slave) |
| I3C | r_i3c | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_i3c) |
| CAN | r_can | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_can) |
| CAN-FD | r_canfd | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_canfd) |
| Ethernet MAC | r_ether | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ether) |
| Ethernet PHY | r_ether_phy | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ether_phy) |
| USB (Basic) | r_usb_basic | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_basic) |
| Camera Engine Unit | r_ceu | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ceu) |
| MIPI CSI | r_mipi_csi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_mipi_csi) |
| Graphics LCD Controller | r_glcdc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_glcdc) |
| 2D Drawing Engine | r_drw | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_drw) |
| JPEG Codec | r_jpeg | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_jpeg) |
| Capacitive Touch Sensing Unit | r_ctsu | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ctsu) |
| Code Flash / Data Flash (HP) | r_flash_hp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_flash_hp) |
| Code Flash / Data Flash (LP) | r_flash_lp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_flash_lp) |
| DMA Controller | r_dmac | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dmac) |
| Data Transfer Controller | r_dtc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dtc) |
| Clock Generation Circuit | r_cgc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_cgc) |
| Clock Accuracy Circuit | r_cac | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_cac) |
| Low Power Modes | r_lpm | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_lpm) |
| Independent Watchdog | r_iwdt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iwdt) |
| I/O Port | r_ioport | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ioport) |
| External IRQ | r_icu | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_icu) |
| Bluetooth LE | r_ble | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ble) |

> The complete list of peripheral HAL driver modules is available in [`ra/fsp/src`](https://github.com/renesas/fsp/tree/master/ra/fsp/src).

## Renesas BSP Board Support

The BSP provides board-specific initialization, pin configuration and peripheral mapping. Each supported RA development kit has a board definition folder inside the FSP repository, named `<device>_<kittype>` (e.g., `ra8d1_ek`, `ra6m5_ck`, `ra8t1_mck`). Board-specific examples live in [ra-fsp-examples](https://github.com/renesas/ra-fsp-examples).

| Board | BSP folder | Repository |
| :--- | :--- | :--- |
| EK-RA2A1 | ra2a1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2a1_ek) |
| EK-RA2E1 | ra2e1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2e1_ek) |
| EK-RA2L1 | ra2l1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2l1_ek) |
| EK-RA4M1 | ra4m1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4m1_ek) |
| EK-RA4M2 | ra4m2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4m2_ek) |
| EK-RA4M3 | ra4m3_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4m3_ek) |
| EK-RA4W1 | ra4w1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4w1_ek) |
| EK-RA6M1 | ra6m1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m1_ek) |
| EK-RA6M2 | ra6m2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m2_ek) |
| EK-RA6M3 | ra6m3_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m3_ek) |
| EK-RA6M3G | ra6m3g_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m3g_ek) |
| EK-RA6M4 | ra6m4_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m4_ek) |
| EK-RA6M5 | ra6m5_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m5_ek) |
| CK-RA6M5 | ra6m5_ck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m5_ck) |
| EK-RA8D1 | ra8d1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8d1_ek) |
| EK-RA8M1 | ra8m1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8m1_ek) |
| VK-RA8M1 | ra8m1_vk | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8m1_vk) |
| EK-RA8P1 | ra8p1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8p1_ek) |
| MCK-RA8T1 | ra8t1_mck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8t1_mck) |
| MCK-RA6T2 | ra6t2_mck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6t2_mck) |
| FPB-RA0E1 | ra0e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra0e1_fpb) |
| FPB-RA2E1 | ra2e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2e1_fpb) |
| FPB-RA4E1 | ra4e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4e1_fpb) |
| FPB-RA6E1 | ra6e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6e1_fpb) |
| FPB-RA8E1 | ra8e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8e1_fpb) |

> The complete list of supported board folders is available in [`ra/board`](https://github.com/renesas/fsp/tree/master/ra/board).

## Renesas MW Libraries and Applications

Middleware libraries provide software modules handling communication, file systems, RTOS, security and graphics. Renesas-tuned middleware is delivered either inside FSP (as `rm_*` module folders) or, for third-party stacks, as dedicated Renesas forks.

| Middleware | Description | Repository |
| :--- | :--- | :--- |
| lwIP | TCP/IP networking stack (Renesas fork) | [Go to repository](https://github.com/renesas/lwip) |
| Mbed TLS | SSL/TLS and crypto library (Renesas fork) | [Go to repository](https://github.com/renesas/mbedtls) |
| TF-PSA-Crypto | PSA Cryptography API reference implementation (Renesas fork) | [Go to repository](https://github.com/renesas/TF-PSA-Crypto) |
| Trusted Firmware-M | TF-M secure firmware for Armv8-M TrustZone | [Go to repository](https://github.com/renesas/trusted-firmware-m) |
| MCUboot | Secure bootloader for 32-bit MCUs (Renesas fork) | [Go to repository](https://github.com/renesas/mcuboot) |
| LVGL | Embedded graphics library (Renesas fork) | [Go to repository](https://github.com/renesas/lvgl) |
| minimp3 | Minimalistic MP3 decoder (Renesas fork) | [Go to repository](https://github.com/renesas/minimp3) |
| Zephyr RTOS | Zephyr Project primary tree (Renesas fork) | [Go to repository](https://github.com/renesas/zephyr) |
| Zephyr HAL (hal_renesas) | HAL for Renesas devices in the Zephyr Project | [Go to repository](https://github.com/renesas/hal_renesas) |
| NuttX | Apache NuttX RTOS (Renesas fork) | [Go to repository](https://github.com/renesas/nuttx) |
| MicroPython | MicroPython for Renesas MCUs | [Go to repository](https://github.com/renesas/micropython) |

## Renesas AI and Model Deployment

The Renesas AI toolchain converts, optimizes and deploys trained models onto RA/RX MCUs and RZ MPUs.

| Component | Description | Repository |
| :--- | :--- | :--- |
| RUHMI Framework (MCU) | AI model optimization and deployment for MCUs, powered by EdgeCortix® MERA™ | [Go to repository](https://github.com/renesas/ruhmi-framework-mcu) |
| RUHMI Framework (RZ/G) | AI model compiler workflow for RZ/G3E | [Go to repository](https://github.com/renesas/ruhmi-framework-rzg) |
| RUHMI Model Zoo | AI/ML model zoo, optimized models and application examples for Renesas platforms | [Go to repository](https://github.com/renesas/ruhmi-model-zoo) |

## Renesas Utilities and miscellaneous

These repositories provide tools and resources to assist development with Renesas microcontrollers.

| Utility | Description | Repository |
| :--- | :--- | :--- |
| Smart Configurator Data | Data repository for the Smart Configurator (SC) tool | [Go to repository](https://github.com/renesas/smart-configurator-data) |
| CMSIS-View | Software event generation and I/O handling tooling | [Go to repository](https://github.com/renesas/CMSIS-View) |
| RZ/A Initial Program Loader | Initial Program Loader (IPL) for RZ/A MPU | [Go to repository](https://github.com/renesas/rza-initial-program-loader) |
