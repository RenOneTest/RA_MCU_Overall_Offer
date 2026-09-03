# Renesas FSP-based Embedded Software

> [!IMPORTANT]
> Unlike a modular multi-repository model, the Renesas RA software offer is delivered through a **monorepo model**: the Flexible Software Package (FSP) HAL drivers, Board Support Packages (BSP), CMSIS device headers, and most middleware are all maintained inside a single repository, [`renesas/fsp`](https://github.com/renesas/fsp). The tables below link directly to the relevant folder inside that repository, or to the dedicated repository where one exists (examples, RX/RZ packages, middleware, AI).

## Table of contents

- [Renesas FSP MCU Packages](#renesas-fsp-mcu-packages)
- [Renesas Application Projects and Examples](#renesas-application-projects-and-examples)
- [Renesas CMSIS](#renesas-cmsis)
- [Renesas FSP HAL Drivers](#renesas-fsp-hal-drivers)
- [Renesas Sensor Middleware](#renesas-sensor-middleware)
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

The HAL Drivers propose the HAL and register-level driver modules controlling all the hardware peripherals embedded in the Renesas RA products. Each peripheral driver is maintained as a module folder (`r_<peripheral>`) inside the FSP repository, under [`ra/fsp/src`](https://github.com/renesas/fsp/tree/master/ra/fsp/src). The modules below are grouped by functional category, matching the FSP module taxonomy. Their usage is illustrated through examples in the [ra-fsp-examples](https://github.com/renesas/ra-fsp-examples) repository.

### Analog

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| ADC (ADC12/14/16) | r_adc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_adc) |
| ADC (ADC_B) | r_adc_b | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_adc_b) |
| ADC (ADC_D, ADC10/12) | r_adc_d | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_adc_d) |
| Sigma-Delta ADC (SDADC24) | r_sdadc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sdadc) |
| Sigma-Delta ADC (SDADC_B) | r_sdadc_b | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sdadc_b) |
| DAC (DAC12) | r_dac | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dac) |
| DAC8 | r_dac8 | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dac8) |
| DAC (DAC_B) | r_dac_b | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dac_b) |
| Comparator, High-Speed (ACMPHS) | r_acmphs | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_acmphs) |
| Comparator, High-Speed (ACMPHS_B) | r_acmphs_b | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_acmphs_b) |
| Comparator, Low-Power (ACMPLP) | r_acmplp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_acmplp) |
| Operational Amplifier (OPAMP) | r_opamp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_opamp) |
| Delta-Sigma Modulator Interface (DSMIF) | r_dsmif | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dsmif) |

### Timers

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| General PWM Timer (GPT) | r_gpt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_gpt) |
| Three-Phase PWM (GPT) | r_gpt_three_phase | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_gpt_three_phase) |
| Asynchronous General-Purpose Timer (AGT) | r_agt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_agt) |
| Timer Array Unit (TAU) | r_tau | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_tau) |
| TAU PWM | r_tau_pwm | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_tau_pwm) |
| 32-bit Interval Timer (TML) | r_tml | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_tml) |
| Ultra-Low-Power Timer (ULPT) | r_ulpt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ulpt) |
| Port Output Enable for GPT (POEG) | r_poeg | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_poeg) |
| Realtime Clock (RTC) | r_rtc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_rtc) |
| Realtime Clock (RTC_C) | r_rtc_c | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_rtc_c) |

### Connectivity — Serial (UART / SPI / I2C / LIN)

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| SCI UART | r_sci_uart | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_uart) |
| SCI_B UART | r_sci_b_uart | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_b_uart) |
| SCI SPI | r_sci_spi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_spi) |
| SCI_B SPI | r_sci_b_spi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_b_spi) |
| SCI I2C | r_sci_i2c | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_i2c) |
| SCI_B I2C | r_sci_b_i2c | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_b_i2c) |
| SCI Smart Card Interface | r_sci_smci | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_smci) |
| SCI LIN | r_sci_lin | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_lin) |
| SCI_B LIN | r_sci_b_lin | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sci_b_lin) |
| SAU UART | r_sau_uart | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sau_uart) |
| SAU SPI | r_sau_spi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sau_spi) |
| SAU I2C | r_sau_i2c | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sau_i2c) |
| SAU LIN | r_sau_lin | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sau_lin) |
| UARTA | r_uarta | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_uarta) |
| SPI | r_spi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_spi) |
| SPI_B | r_spi_b | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_spi_b) |
| I2C Master (IIC) | r_iic_master | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iic_master) |
| I2C Slave (IIC) | r_iic_slave | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iic_slave) |
| I2C Master (IIC_B) | r_iic_b_master | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iic_b_master) |
| I2C Slave (IIC_B) | r_iic_b_slave | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iic_b_slave) |
| I2C Master (IICA) | r_iica_master | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iica_master) |
| I2C Slave (IICA) | r_iica_slave | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iica_slave) |
| I3C | r_i3c | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_i3c) |

### Connectivity — CAN / CEC / Camera

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| CAN | r_can | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_can) |
| CAN-FD | r_canfd | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_canfd) |
| Consumer Electronics Control (CEC) | r_cec | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_cec) |
| Camera Engine Unit (CEU) | r_ceu | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ceu) |

### Connectivity — USB

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| USB Basic | r_usb_basic | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_basic) |
| USB Composite | r_usb_composite | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_composite) |
| USB Host CDC | r_usb_hcdc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_hcdc) |
| USB Host CDC-ECM | r_usb_hcdc_ecm | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_hcdc_ecm) |
| USB Host HID | r_usb_hhid | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_hhid) |
| USB Host MSC | r_usb_hmsc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_hmsc) |
| USB Host UVC | r_usb_huvc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_huvc) |
| USB Host Audio | r_usb_haud | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_haud) |
| USB Peripheral CDC | r_usb_pcdc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_pcdc) |
| USB Peripheral HID | r_usb_phid | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_phid) |
| USB Peripheral MSC | r_usb_pmsc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_pmsc) |
| USB Peripheral Audio | r_usb_paud | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_paud) |
| USB Peripheral Printer | r_usb_pprn | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_pprn) |
| USB Peripheral UVC | r_usb_puvc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_puvc) |
| USB Peripheral Vendor | r_usb_pvnd | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_pvnd) |
| USB Type-C | r_usb_typec | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_usb_typec) |

### Networking

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| Ethernet MAC | r_ether | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ether) |
| Ethernet PHY | r_ether_phy | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ether_phy) |
| EtherCAT PHY | r_ethercat_phy | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ethercat_phy) |
| Gigabit Ethernet MAC (RMAC) | r_rmac | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_rmac) |
| RMAC PHY | r_rmac_phy | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_rmac_phy) |
| Generic Timer PTP (gPTP) | r_gptp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_gptp) |
| Precision Time Protocol (PTP) | r_ptp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ptp) |
| Layer 3 Switch | r_layer3_switch | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_layer3_switch) |

### Graphics & Display

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| Graphics LCD Controller (GLCDC) | r_glcdc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_glcdc) |
| 2D Drawing Engine (DRW) | r_drw | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_drw) |
| JPEG Codec | r_jpeg | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_jpeg) |
| MIPI CSI | r_mipi_csi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_mipi_csi) |
| MIPI DSI | r_mipi_dsi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_mipi_dsi) |
| MIPI PHY | r_mipi_phy | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_mipi_phy) |
| Segment LCD Controller (SLCDC) | r_slcdc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_slcdc) |
| Parallel Data Capture (PDC) | r_pdc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_pdc) |
| Video Input (VIN) | r_vin | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_vin) |

### Audio

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| Serial Sound Interface (SSI) | r_ssi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ssi) |
| PDM Interface | r_pdm | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_pdm) |

### Storage & Memory

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| SD/MMC Host Interface (SDHI) | r_sdhi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sdhi) |
| Octal-SPI (OSPI) | r_ospi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ospi) |
| Octal-SPI (OSPI_B) | r_ospi_b | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ospi_b) |
| Quad-SPI (QSPI) | r_qspi | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_qspi) |
| Code Flash / Data Flash (HP) | r_flash_hp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_flash_hp) |
| Code Flash / Data Flash (LP) | r_flash_lp | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_flash_lp) |
| MRAM | r_mram | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_mram) |

### DSP, CapTouch & Input

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| IIR Filter Accelerator (IIRFA) | r_iirfa | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iirfa) |
| Capacitive Touch Sensing Unit (CTSU) | r_ctsu | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ctsu) |
| Key Interrupt (KINT) | r_kint | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_kint) |

### Security

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| Secure Crypto Engine (SCE) | r_sce | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sce) |
| SCE Protected Mode | r_sce_protected | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sce_protected) |
| SCE Key Injection | r_sce_key_injection | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_sce_key_injection) |
| RSIP Protected Mode | r_rsip_protected | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_rsip_protected) |
| RSIP Key Injection | r_rsip_key_injection | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_rsip_key_injection) |

### Monitoring & Safety

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| CRC Calculator | r_crc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_crc) |
| Data Operation Circuit (DOC) | r_doc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_doc) |
| Clock Frequency Accuracy Measurement Circuit (CAC) | r_cac | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_cac) |
| Low Voltage Detection (LVD) | r_lvd | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_lvd) |
| Independent Watchdog (IWDT) | r_iwdt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_iwdt) |
| Watchdog (WDT) | r_wdt | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_wdt) |

### System & Transfer

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| Clock Generation Circuit (CGC) | r_cgc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_cgc) |
| Interrupt Controller Unit (ICU) | r_icu | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_icu) |
| Event Link Controller (ELC) | r_elc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_elc) |
| I/O Port | r_ioport | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ioport) |
| Low Power Modes (LPM) | r_lpm | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_lpm) |
| Inter-Processor Communication (IPC) | r_ipc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ipc) |
| DMA Controller (DMAC) | r_dmac | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dmac) |
| Data Transfer Controller (DTC) | r_dtc | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_dtc) |

### Wireless

| Peripheral | HAL Driver module | Repository |
| :--- | :--- | :--- |
| Bluetooth LE | r_ble | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/r_ble) |

> The complete, authoritative list of peripheral HAL driver modules is maintained in [`ra/fsp/src`](https://github.com/renesas/fsp/tree/master/ra/fsp/src). Not all modules are available for all MCUs — see the [Module Support by Device](https://renesas.github.io/fsp/group___r_e_n_e_s_a_s___m_o_d_u_l_e_s.html) table in the FSP documentation.

## Renesas Sensor Middleware

Renesas sensor drivers are delivered as FSP middleware modules (`rm_<part>`) inside the FSP repository, providing hardware-abstracted access to Renesas sensor devices over I2C/SPI.

| Sensor | Middleware module | Repository |
| :--- | :--- | :--- |
| HS300x Relative Humidity & Temperature | rm_hs300x | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_hs300x) |
| HS400x Relative Humidity & Temperature | rm_hs400x | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_hs400x) |
| FS3000 Air Flow | rm_fs3000 | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_fs3000) |
| ZMOD4xxx Gas Sensor | rm_zmod4xxx | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_zmod4xxx) |
| RRH62000 Air Quality | rm_rrh62000 | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_rrh62000) |
| RRH46410 Gas Sensor | rm_rrh46410 | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_rrh46410) |
| RRH47000 Gas Sensor | rm_rrh47000 | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_rrh47000) |
| Touch (CTSU middleware) | rm_touch | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_touch) |
| Comms I2C bus abstraction | rm_comms_i2c | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/fsp/src/rm_comms_i2c) |

## Renesas BSP Board Support

The BSP provides board-specific initialization, pin configuration and peripheral mapping. Each supported RA development kit has a board definition folder inside the FSP repository, named `<device>_<kittype>` (e.g., `ra8d1_ek`, `ra6m5_ck`, `ra8t1_mck`). Board-specific examples live in [ra-fsp-examples](https://github.com/renesas/ra-fsp-examples). The full list of board folders is browsable at [`ra/board`](https://github.com/renesas/fsp/tree/master/ra/board).

### RA0 Series (Entry-Line)

| Board | BSP folder | Repository |
| :--- | :--- | :--- |
| FPB-RA0E1 | ra0e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra0e1_fpb) |
| FPB-RA0E2 | ra0e2_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra0e2_fpb) |
| FPB-RA0E3 | ra0e3_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra0e3_fpb) |
| FPB-RA0L1 | ra0l1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra0l1_fpb) |
| RSSK-RA0L1 | ra0l1_rssk | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra0l1_rssk) |

### RA2 Series (General-Purpose)

| Board | BSP folder | Repository |
| :--- | :--- | :--- |
| EK-RA2A1 | ra2a1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2a1_ek) |
| EK-RA2A2 | ra2a2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2a2_ek) |
| EK-RA2E1 | ra2e1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2e1_ek) |
| FPB-RA2E1 | ra2e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2e1_fpb) |
| EK-RA2E2 | ra2e2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2e2_ek) |
| FPB-RA2E2 | ra2e2_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2e2_fpb) |
| FPB-RA2E3 | ra2e3_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2e3_fpb) |
| EK-RA2L1 | ra2l1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2l1_ek) |
| RSSK-RA2L1 | ra2l1_rssk | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2l1_rssk) |
| VOICE-RA2L1 | ra2l1_voice | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2l1_voice) |
| EK-RA2L2 | ra2l2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2l2_ek) |
| FPB-RA2T1 | ra2t1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra2t1_fpb) |

### RA4 Series (Mainstream)

| Board | BSP folder | Repository |
| :--- | :--- | :--- |
| EK-RA4C1 | ra4c1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4c1_ek) |
| FPB-RA4E1 | ra4e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4e1_fpb) |
| VOICE-RA4E1 | ra4e1_voice | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4e1_voice) |
| EK-RA4E2 | ra4e2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4e2_ek) |
| FPB-RA4E2 | ra4e2_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4e2_fpb) |
| EK-RA4L1 | ra4l1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4l1_ek) |
| RSSK-RA4L1 | ra4l1_rssk | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4l1_rssk) |
| EK-RA4M1 | ra4m1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4m1_ek) |
| EK-RA4M2 | ra4m2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4m2_ek) |
| EK-RA4M3 | ra4m3_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4m3_ek) |
| MCK-RA4T1 | ra4t1_mck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4t1_mck) |
| EK-RA4W1 | ra4w1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra4w1_ek) |

### RA6 Series (High-Performance)

| Board | BSP folder | Repository |
| :--- | :--- | :--- |
| FPB-RA6E1 | ra6e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6e1_fpb) |
| VOICE-RA6E1 | ra6e1_voice | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6e1_voice) |
| EK-RA6E2 | ra6e2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6e2_ek) |
| FPB-RA6E2 | ra6e2_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6e2_fpb) |
| EK-RA6M1 | ra6m1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m1_ek) |
| EK-RA6M2 | ra6m2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m2_ek) |
| EK-RA6M3 | ra6m3_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m3_ek) |
| EK-RA6M3G | ra6m3g_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m3g_ek) |
| EK-RA6M4 | ra6m4_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m4_ek) |
| CK-RA6M5 | ra6m5_ck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m5_ck) |
| CK-RA6M5 V2 | ra6m5_ck_v2 | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m5_ck_v2) |
| EK-RA6M5 | ra6m5_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6m5_ek) |
| RSSK-RA6T1 | ra6t1_rssk | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6t1_rssk) |
| MCK-RA6T2 | ra6t2_mck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6t2_mck) |
| MCK-RA6T3 | ra6t3_mck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra6t3_mck) |

### RA8 Series (Advanced Performance)

| Board | BSP folder | Repository |
| :--- | :--- | :--- |
| EK-RA8D1 | ra8d1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8d1_ek) |
| EK-RA8D2 | ra8d2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8d2_ek) |
| FPB-RA8E1 | ra8e1_fpb | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8e1_fpb) |
| EK-RA8E2 | ra8e2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8e2_ek) |
| EK-RA8M1 | ra8m1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8m1_ek) |
| VK-RA8M1 | ra8m1_vk | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8m1_vk) |
| EK-RA8M2 | ra8m2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8m2_ek) |
| EK-RA8P1 | ra8p1_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8p1_ek) |
| MCK-RA8T1 | ra8t1_mck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8t1_mck) |
| EK-RA8T2 | ra8t2_ek | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8t2_ek) |
| MCK-RA8T2 | ra8t2_mck | [Go to repository](https://github.com/renesas/fsp/tree/master/ra/board/ra8t2_mck) |

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
