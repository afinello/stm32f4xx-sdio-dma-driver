# stm32f4xx-sdio-dma-driver
STM32F4xx DMA-capable SDIO SD-card driver compatible with FatFs library

This is a modified version of the original STMicroelectronics SDIO driver with DMA-mode working out-of-the-box on STM32F4xx family chips.

Some boards do not have a CD-pin (Card Detect), so you should comment out the following definition in sdio_sd.c file to turn off the SD-card presense validation.

```c
#define SD_USE_DETECT_PIN
```

Add the following definition to your code to enable the Polling mode instead of DMA

```c
#define SD_POLLING_MODE ((uint32_t)0x00000002)
```
