# Renesas FSP-based Embedded Software

## Table of contents

- [Renesas FSP MCU Packages](#renesas-fsp-mcu-packages)
- [Renesas Application Expansion Packages](#renesas-application-expansion-packages)
- [Renesas Function Packs](#renesas-function-packs)
- [Renesas CMSIS](#renesas-cmsis)
- [Renesas FSP HAL Drivers](#renesas-fsp-hal-drivers)
- [Renesas BSP Drivers](#renesas-bsp-drivers)
- [Renesas MW Libraries and Applications](#renesas-mw-libraries-and-applications)
- [Renesas USB-PD Components](#renesas-usb-pd-components)
- [Renesas Utilities and miscellaneous](#renesas-utilities-and-miscellaneous)

## Renesas FSP MCU Packages

Renesas FSP MCU Packages provide embedded software components, including drivers, middleware, and utilities, for developing applications on Renesas RA microcontrollers. Example projects demonstrate their use on Renesas RA boards. Additionally, the Flexible Software Package (FSP) framework ensures portability across the RA series.

| MCU package | Repository |
| :--- | :--- |
| FSP-RA0 | [Go to repository](#) |
| FSP-RA2 | [Go to repository](#) |
| FSP-RA4 | [Go to repository](#) |
| FSP-RA4W1 | [Go to repository](#) |
| FSP-RA6 | [Go to repository](#) |
| FSP-RA8 | [Go to repository](#) |

## Renesas Application Expansion Packages

Renesas Application Expansion Packages complement the FSP MCU Packages with additional software bricks, including specific drivers for external companion chips or application-specific middleware. They offer simplified implementations of real-world use cases in areas, such as sensing, power management, connectivity, and audio.

**Section content**

- [Renesas AI Expansion Package](#renesas-ai-expansion-package)
- [Renesas Azure RTOS Expansion Package](#renesas-azure-rtos-expansion-package)
- [Renesas Connectivity Expansion Package](#renesas-connectivity-expansion-package)
- [Renesas FreeRTOS Expansion Package](#renesas-freertos-expansion-package)
- [Renesas IoT Expansion Package](#renesas-iot-expansion-package)
- [Renesas MEMS and Sensors Expansion Package](#renesas-mems-and-sensors-expansion-package)
- [Renesas USB-PD Expansion Package](#renesas-usb-pd-expansion-package)
- [Renesas Miscellaneous Expansion Package](#renesas-miscellaneous-expansion-package)

### Renesas AI Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-ai-vision-face-detection | [Go to repository](#) |
| ra-ai-hand-gesture-recognition | [Go to repository](#) |
| ra-ai-people-detection-tracking | [Go to repository](#) |
| ra-ai-object-detection | [Go to repository](#) |
| ra-ai-power-measurement | [Go to repository](#) |
| ra-camera-capture | [Go to repository](#) |

### Renesas Azure RTOS Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-azrtos-ra4 | [Go to repository](#) |
| ra-azrtos-ra6 | [Go to repository](#) |
| ra-azrtos-ra8 | [Go to repository](#) |

### Renesas Connectivity Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-ble | [Go to repository](#) |
| ra-nfc | [Go to repository](#) |
| ra-subghz | [Go to repository](#) |
| ra-wifi | [Go to repository](#) |

### Renesas FreeRTOS Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-freertos | [Go to repository](#) |

### Renesas IoT Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-aws | [Go to repository](#) |
| ra-azure-iot | [Go to repository](#) |

### Renesas MEMS and Sensors Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-sensors | [Go to repository](#) |
| ra-mems-mic | [Go to repository](#) |
| ra-tof | [Go to repository](#) |

### Renesas USB-PD Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-usb-pd | [Go to repository](#) |
| ra-tcpp | [Go to repository](#) |

### Renesas Miscellaneous Expansion Package

| Expansion Package | Repository |
| :--- | :--- |
| ra-eeprom | [Go to repository](#) |
| ra-gnss | [Go to repository](#) |

## Renesas Function Packs

Renesas Function Packs (FP) are a combination of low-level drivers, middleware libraries and sample applications assembled into a single software package. You can get the entire list of available Function Packs on [renesas.com](https://www.renesas.com). The below list represents the Function Packs available on github.com.

| Function Pack | Repository |
| :--- | :--- |
| fp-ai-sensing | [Go to repository](#) |
| fp-ai-vision | [Go to repository](#) |
| fp-aud-smartmic | [Go to repository](#) |
| fp-sns-datalog | [Go to repository](#) |
| fp-sns-motenv | [Go to repository](#) |
| fp-cld-azure | [Go to repository](#) |
| fp-cld-aws | [Go to repository](#) |

## Renesas FSP MCU Components

As mentioned above, the Renesas FSP MCU Components are an alternative delivery model to the FSP monolithic offer. Each software component is delivered in a dedicated repository, allowing users to select and download only those relevant to their application needs.

> [!NOTE]
> Care must be taken regarding the cross-compatibility of components. Please refer to the README.md file in each repository for details.

## Renesas CMSIS

The CMSIS interfaces offer access to the Arm Cortex®-M processor core features and device-specific peripherals of Renesas RA microcontrollers.

### Renesas CMSIS Core

| CMSIS Core | Repository |
| :--- | :--- |
| cmsis-core | [Go to repository](#) |

### Renesas CMSIS Device

| CMSIS Device | Repository |
| :--- | :--- |
| cmsis-device-ra0 | [Go to repository](#) |
| cmsis-device-ra2 | [Go to repository](#) |
| cmsis-device-ra4 | [Go to repository](#) |
| cmsis-device-ra4w1 | [Go to repository](#) |
| cmsis-device-ra6 | [Go to repository](#) |
| cmsis-device-ra8 | [Go to repository](#) |

## Renesas FSP HAL Drivers

The HAL Drivers MCU Components propose the HAL and register-level driver modules controlling all the hardware peripherals embedded in the Renesas RA products.

**HAL Drivers:** A set of portable abstraction APIs offering high level services, built around standalone processes. The HAL drivers are functionality-oriented, example: for the Timer peripheral, the APIs could be split into several categories following the functions offered by the IPs (Basic timer, capture, PWM...); for a communication IP: an initialisation function, eventually a configuration function and data transfer services (polling, interruption or DMA based). The compatibility SHALL be guaranteed across all the RA families for the generic APIs, including generic macros and common structure defines. Any specific feature is given in a dedicated extension model available in the associated extension files.

**Register-level Drivers:** A set of basic functions with direct hardware access (no standalone process), this layer can be called either by applications or by the HAL drivers.

Both HAL and register-level drivers of each series are provided in the same repository. Their usage is illustrated through examples, available in the respective Renesas FSP MCU Firmware repositories.

| HAL Driver | Repository |
| :--- | :--- |
| ra0xx-hal-driver | [Go to repository](#) |
| ra2xx-hal-driver | [Go to repository](#) |
| ra4xx-hal-driver | [Go to repository](#) |
| ra4w1xx-hal-driver | [Go to repository](#) |
| ra6xx-hal-driver | [Go to repository](#) |
| ra8xx-hal-driver | [Go to repository](#) |

## Renesas BSP Drivers

The BSP Drivers MCU Components propose the Board Support Package Drivers, which are constituted from the:

- **Renesas BSP Board Drivers**, based on the HAL drivers, and providing a set of high level APIs allowing a quick access to the board services (e.g., audio, graphics, access to external memories).
- **Renesas BSP Component Drivers** providing a set of high level APIs allowing a quick access to hardware components available on the board but external to the MCU (e.g., audio codecs, LCD drivers, SD cards, MEMS). The link between these external components and the HAL drivers (e.g., an SD card and the OSPI / QSPI HAL driver) is established within the BSP Board drivers.

> [!NOTE]
> A number of BSP component drivers (particularly of MEMS) come in two forms, each addressing a different purpose. For each one of such BSP component drivers, two repositories are available as explained below:
>
> - **PID: Platform-Independent Drivers.** Recognizable to their repositories' names `<bspcomp>` (e.g., `hs300x`). Are low-level drivers allowing direct access to components' registers. These drivers are independent of any software platform, as the acronym PID suggests.
> - **RA: FSP-compatible drivers.** Recognizable to their repositories' names `ra-<bspcomp>` (e.g., `ra-hs300x`). Are hardware-abstracted drivers, specially designed to be compatible with the Renesas FSP software offer, as the `ra-` prefix suggests.

### Renesas BSP Board Drivers

**Section content**

- [FSP-RA0 BSP Boards Drivers](#fsp-ra0-bsp-boards-drivers)
- [FSP-RA2 BSP Boards Drivers](#fsp-ra2-bsp-boards-drivers)
- [FSP-RA4 BSP Boards Drivers](#fsp-ra4-bsp-boards-drivers)
- [FSP-RA4W1 BSP Boards Drivers](#fsp-ra4w1-bsp-boards-drivers)
- [FSP-RA6 BSP Boards Drivers](#fsp-ra6-bsp-boards-drivers)
- [FSP-RA8 BSP Boards Drivers](#fsp-ra8-bsp-boards-drivers)

#### FSP-RA0 BSP Boards Drivers

| BSP Board Driver | Repository |
| :--- | :--- |
| ek-ra0e1-bsp | [Go to repository](#) |
| fpb-ra0e1-bsp | [Go to repository](#) |

#### FSP-RA2 BSP Boards Drivers

| BSP Board Driver | Repository |
| :--- | :--- |
| ek-ra2a1-bsp | [Go to repository](#) |
| ek-ra2e1-bsp | [Go to repository](#) |
| ek-ra2e2-bsp | [Go to repository](#) |
| ek-ra2l1-bsp | [Go to repository](#) |
| fpb-ra2e3-bsp | [Go to repository](#) |

#### FSP-RA4 BSP Boards Drivers

| BSP Board Driver | Repository |
| :--- | :--- |
| ek-ra4e2-bsp | [Go to repository](#) |
| ek-ra4m1-bsp | [Go to repository](#) |
| ek-ra4m2-bsp | [Go to repository](#) |
| ek-ra4m3-bsp | [Go to repository](#) |
| ek-ra4w1-bsp | [Go to repository](#) |
| fpb-ra4e1-bsp | [Go to repository](#) |

#### FSP-RA4W1 BSP Boards Drivers

| BSP Board Driver | Repository |
| :--- | :--- |
| ek-ra4w1-bsp | [Go to repository](#) |

#### FSP-RA6 BSP Boards Drivers

| BSP Board Driver | Repository |
| :--- | :--- |
| ek-ra6e2-bsp | [Go to repository](#) |
| ek-ra6m1-bsp | [Go to repository](#) |
| ek-ra6m2-bsp | [Go to repository](#) |
| ek-ra6m3-bsp | [Go to repository](#) |
| ek-ra6m3g-bsp | [Go to repository](#) |
| ek-ra6m4-bsp | [Go to repository](#) |
| ek-ra6m5-bsp | [Go to repository](#) |
| fpb-ra6e1-bsp | [Go to repository](#) |
| fpb-ra6e2-bsp | [Go to repository](#) |

#### FSP-RA8 BSP Boards Drivers

| BSP Board Driver | Repository |
| :--- | :--- |
| ek-ra8d1-bsp | [Go to repository](#) |
| ek-ra8m1-bsp | [Go to repository](#) |
| fpb-ra8e1-bsp | [Go to repository](#) |
| mck-ra8t1-bsp | [Go to repository](#) |

### Renesas BSP Component Drivers

**Section content**

- [Renesas BSP Audio Component Drivers](#renesas-bsp-audio-component-drivers)
- [Renesas BSP BLE Component Drivers](#renesas-bsp-ble-component-drivers)
- [Renesas BSP Camera Component Drivers](#renesas-bsp-camera-component-drivers)
- [Renesas BSP Display Component Drivers](#renesas-bsp-display-component-drivers)
- [Renesas BSP EEPROM Component Drivers](#renesas-bsp-eeprom-component-drivers)
- [Renesas BSP IO Expander Component Drivers](#renesas-bsp-io-expander-component-drivers)
- [Renesas BSP LCD Component Drivers](#renesas-bsp-lcd-component-drivers)
- [Renesas BSP MEMS Component Drivers](#renesas-bsp-mems-component-drivers)
- [Renesas BSP Networking Component Drivers](#renesas-bsp-networking-component-drivers)
- [Renesas BSP NFC/RFID Tag Component Drivers](#renesas-bsp-nfcrfid-tag-component-drivers)
- [Renesas BSP xSPI-Interfaced Memory Component Drivers](#renesas-bsp-xspi-interfaced-memory-component-drivers)
- [Renesas BSP SDRAM Component Drivers](#renesas-bsp-sdram-component-drivers)
- [Renesas BSP Temperature and Humidity Sensor Component Drivers](#renesas-bsp-temperature-and-humidity-sensor-component-drivers)
- [Renesas BSP Touch Screen Component Drivers](#renesas-bsp-touch-screen-component-drivers)
- [Renesas BSP USB-C Component Drivers](#renesas-bsp-usb-c-component-drivers)
- [Renesas BSP Wi-Fi Component Drivers](#renesas-bsp-wi-fi-component-drivers)

#### Renesas BSP Audio Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-da7212 | [Go to repository](#) |
| ra-wm8978 | [Go to repository](#) |

#### Renesas BSP BLE Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-da14531 | [Go to repository](#) |

#### Renesas BSP Camera Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-ov3640 | [Go to repository](#) |
| ra-ov5640 | [Go to repository](#) |

#### Renesas BSP Display Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-sn65dsi | [Go to repository](#) |

#### Renesas BSP EEPROM Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-r1ex24 | [Go to repository](#) |

#### Renesas BSP IO Expander Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-pcal6408 | [Go to repository](#) |

#### Renesas BSP LCD Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-ili9341 | [Go to repository](#) |
| ra-st7789 | [Go to repository](#) |
| ra-gt911 | [Go to repository](#) |

#### Renesas BSP MEMS Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-icm42605 | [Go to repository](#) |
| ra-icp10101 | [Go to repository](#) |
| ra-zmod4410 | [Go to repository](#) |

#### Renesas BSP Networking Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-dp83848 | [Go to repository](#) |
| ra-ksz8091 | [Go to repository](#) |

#### Renesas BSP NFC/RFID Tag Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-st25dv | [Go to repository](#) |

#### Renesas BSP xSPI-Interfaced Memory Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-mx25l | [Go to repository](#) |
| ra-mx25um | [Go to repository](#) |
| ra-at25 | [Go to repository](#) |

#### Renesas BSP SDRAM Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-is42s16 | [Go to repository](#) |

#### Renesas BSP Temperature and Humidity Sensor Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-hs300x | [Go to repository](#) |
| ra-hs400x | [Go to repository](#) |

#### Renesas BSP Touch Screen Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-ft5x06 | [Go to repository](#) |
| ra-gt911 | [Go to repository](#) |

#### Renesas BSP USB-C Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-tcpp01 | [Go to repository](#) |

#### Renesas BSP Wi-Fi Component Drivers

| BSP Component Driver | Repository |
| :--- | :--- |
| ra-da16200 | [Go to repository](#) |
| ra-ry-wifi | [Go to repository](#) |

## Renesas MW Libraries and Applications

Middleware libraries provide software modules that handle common functions like communication, file systems, real-time operating systems (RTOS), and graphics, simplifying application development across Renesas RA microcontrollers.

**Section content**

- [Renesas Classic Core MW Libraries](#renesas-classic-core-mw-libraries)
- [Renesas Azure RTOS MW Libraries](#renesas-azure-rtos-mw-libraries)
- [Renesas Miscellaneous MW Libraries](#renesas-miscellaneous-mw-libraries)
- [Renesas Classic Core MW Applications](#renesas-classic-core-mw-applications)
- [Renesas Secure Bootloader MW Applications](#renesas-secure-bootloader-mw-applications)

### Renesas Classic Core MW Libraries

| Middleware library | Repository |
| :--- | :--- |
| ra-mw-fatfs | [Go to repository](#) |
| ra-mw-freertos | [Go to repository](#) |
| ra-mw-lwip | [Go to repository](#) |
| ra-mw-usb-device | [Go to repository](#) |
| ra-mw-usb-host | [Go to repository](#) |

### Renesas Azure RTOS MW Libraries

| Middleware library | Repository |
| :--- | :--- |
| ra-mw-threadx | [Go to repository](#) |
| ra-mw-filex | [Go to repository](#) |
| ra-mw-levelx | [Go to repository](#) |
| ra-mw-netxduo | [Go to repository](#) |
| ra-mw-usbx | [Go to repository](#) |
| ra-mw-guix | [Go to repository](#) |

### Renesas Miscellaneous MW Libraries

| Middleware library | Repository |
| :--- | :--- |
| ra-mw-mbedtls | [Go to repository](#) |
| ra-mw-mcuboot | [Go to repository](#) |
| ra-mw-lorawan | [Go to repository](#) |
| ra-mw-tinymaix | [Go to repository](#) |
| ra-mw-tfm | [Go to repository](#) |

### Renesas Classic Core MW Applications

| Middleware application | Repository |
| :--- | :--- |
| ra6-classic-coremw-apps | [Go to repository](#) |
| ra8-classic-coremw-apps | [Go to repository](#) |

### Renesas Secure Bootloader MW Applications

| Middleware application | Repository |
| :--- | :--- |
| ra4-secureboot-apps | [Go to repository](#) |
| ra6-secureboot-apps | [Go to repository](#) |
| ra8-secureboot-apps | [Go to repository](#) |

## Renesas USB-PD Components

The USB Power Delivery (USB-PD) software stack includes middleware, BSP drivers, and utilities such as debugging tools, providing a comprehensive solution for USB Power Delivery implementation.

**Section content**

- [Renesas USB-PD MW Libraries](#renesas-usb-pd-mw-libraries)
- [Renesas USB-PD BSP Component Drivers](#renesas-usb-pd-bsp-component-drivers)
- [Renesas USB-PD Utilities](#renesas-usb-pd-utilities)

### Renesas USB-PD MW Libraries

| Middleware library | Repository |
| :--- | :--- |
| ra-mw-usbpd-core | [Go to repository](#) |
| ra-mw-usbpd-device-ra4 | [Go to repository](#) |
| ra-mw-usbpd-device-ra6 | [Go to repository](#) |
| ra-mw-usbpd-ucsi | [Go to repository](#) |

### Renesas USB-PD BSP Component Drivers

| BSP component driver | Repository |
| :--- | :--- |
| ra-bsp-usbpd-tcpp01 | [Go to repository](#) |

### Renesas USB-PD Utilities

| Utility | Repository |
| :--- | :--- |
| ra-util-usbpd-tracer | [Go to repository](#) |

## Renesas Utilities and miscellaneous

These repositories provide tools and resources to assist development with Renesas RA microcontrollers.

| Utility and miscellaneous | Repository |
| :--- | :--- |
| ra-external-loader | [Go to repository](#) |
| ra-ai-tools | [Go to repository](#) |
| RA_open_pin_data | [Go to repository](#) |
