# SN74LV8153
Arduino UNO library for Serial to Parallel Interface SN74LV8153 chip</br>
ref. datasheet: https://www.ti.com/lit/ds/symlink/sn74lv8153.pdf?ts=1707143795904&ref_url=https%253A%252F%252Fwww.google.com%252F

Use:
```
S2PI decoder;
decoder.begin([serial_pin], [reset_pin]);
```
or
```
S2PI decoder([serial_pin], [reset pin]);
```
To write to the device:
```
decoder.output([device_address (pin programmed, ref. datasheet)], [8 bit data]);
```
To reset the device (optional, reset's all pins, ref. datasheet):
```
decoder.reset();
```

</br>
Example:
```
#include "SN74LV8153.h"

S2PI decoder;
const uint8_t serial_pin = 2;
const uint8_t reset_pin = 3;
const uint8_t device_address = 0;      //set by pin programming, ref. datasheet

void setup(){
  decoder.begin(serial_pin, reset_pin);
}

void loop(){
  uint8_t data = 0xff;    //8-bit data to send to chip

  decoder.output(device_address, data);

  while(1);
}
```
