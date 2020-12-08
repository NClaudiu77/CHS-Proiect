# AI APLICATIONS ON EMBEDDED SYSTEMS

## MAIXDUINO - What it is?
Maixduino is a RISC-V 64 development board for AI + IoT applications running on a very powerful embedded AIOT chip [K210]
https://www.seeedstudio.com/Sipeed-Maixduino-Kit-for-RISC-V-AI-IoT-p-4047.html

> K210 brief: 
> * Image Recognition with hardware acceleration
> * Dual core with FPU
> * 8MB(6MB+2MB) RAM
> * 16MB external Flash
> * Max 800MHz CPU freq (see the dev board in detail, usually 400MHz)
> * Microphone array(8 mics)
> * Hardware AES SHA256
> * FPIOA (Peripherals can map to any pins)
> * Peripherals: I2C, SPI, I2S, WDT, TIMER, RTC, UART, GPIO etc.


## What it can do?

> * Image classification
> * Object detection(for example: face detection)
> * Speech recognition
> * Computer vision application like scanning qr-codes, barcodes
> * AI+IOT applications

For more info : https://maixpy.sipeed.com/en/others/what_maix_do.html

## What is MaixPy?
> * MaixPy ported Micropython to K210 (a 64-bit dual-core RISC-V CPU with hardware FPU,FFT,sha256 and convolution accelerator)
> * Maixpy is designed to make AIOT programming easier, based on the Micropython syntax, running on a very powerful embedded AIOT chip K210.
> * For more info: https://github.com/sipeed/MaixPy

## Taking a picture
```
import sensor
import image
import lcd

lcd.init()
sensor.reset()
sensor.set_pixformat(sensor.RGB565)
sensor.set_framesize(sensor.QVGA)
sensor.run(1)
while True:
    img=sensor.snapshot()
    lcd.display(img)
```

For more code examples: 
https://github.com/sipeed/MaixPy_scripts

<div align="center"
<p> Maixduino is specialized to run convolutional neural networks. There are just some formats accepted like Tensorflow Lite and Caffe: </p>
<img src = "https://github.com/kendryte/nncase/blob/master/docs/arch.png" alt="nncase arch" />
</div>

## There are some constraints which models should respect.
> * How to train, convert, run models on Sipeed MaixPy and Maixduino https://blog.sipeed.com/p/680.html
> * Toolbox for converting models :https://github.com/sipeed/Maix_Toolbox
> * https://github.com/kendryte/nncase/tree/v0.1.0-rc5

