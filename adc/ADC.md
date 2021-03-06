# ADC
![adc](http://www.beis.de/Elektronik/DeltaSigma/ADCSinus.GIF)

## Theory

[How sigma/delta ADCs work](http://www.beis.de/Elektronik/DeltaSigma/DeltaSigma.html)


## Arduino

[example for arduino (code and assembly) with ads1x15](https://learn.adafruit.com/adafruit-4-channel-adc-breakouts/overview)

## Raspberry

### Code
[example with 3008](http://www.electroensaimada.com/adc.html)

[example with ads1x15](https://github.com/adafruit/Adafruit-Raspberry-Pi-Python-Code/tree/master/Adafruit_ADS1x15)

[example with MCP3424](https://github.com/abelectronicsuk/ABElectronics_Python_Libraries/tree/master/ADCPi)

[tutorial LTC2309 (C code)](http://www.cooking-hacks.com/documentation/tutorials/raspberry-pi-to-arduino-shields-connection-bridge)


## SMT32

[miniscope (USB oscilloscope) 2x461kSps](http://tomeko.net/miniscope_v2c/index.php?lang=en)

[doc](https://github.com/javacasm/elcacharreo_static/blob/master/_posts/2015-04-23-STM32.md)

### Modules

#### ADC

Description|Bits|Channels|Price|Chip|sps|PGA|Datasheet
---|---|---|---|---|---|---|---
[Deltha Sigma Pi](https://www.abelectronics.co.uk/products/3/Raspberry-Pi/14/Delta-Sigma-Pi)|18|8|18 £|[MCP3424](http://www.microchip.com/wwwproducts/Devices.aspx?product=MCP3424)|3.7(18),240(12)|No|[Datasheet](http://ww1.microchip.com/downloads/en/DeviceDoc/22088c.pdf)
[ADS1115](http://www.adafruit.com/product/1085)|16|4|$14.95||860|Yes x16|[DataSheet](http://www.adafruit.com/datasheets/ads1115.pdf)
[ADS1015](http://www.adafruit.com/products/1083)|12|4|$9.95||3300|Yes x16|[Datasheet](http://adafruit.com/datasheets/ads1015.pdf)
[LTC2309](http://www.linear.com/product/LTC2309)|12|8||14ksps|No|[Datasheet](http://www.linear.com/docs/25786)

#### DAC

[ADC+DAC Pi](https://www.abelectronics.co.uk/products/3/Raspberry-Pi/39/ADC-DAC-Pi-Raspberry-Pi-ADC-and-DAC-expansion-board) 2 ADC 12 bits channels (MCP3202) &  2 DAC 12 bits channels (MCP4822)


#### Addons
Description|Price|Chip
---|---|---
[RTC Pi](https://www.abelectronics.co.uk/products/3/Raspberry-Pi/15/RTC-Pi)|12 £|[DS1307](datasheets.maximintegrated.com/en/ds/DS1307.pdf)
