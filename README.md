# SN74LV8153
Arduino UNO library for Serial to Parallel Interface SN74LV8153 chip
ref. datasheet: https://www.ti.com/lit/ds/symlink/sn74lv8153.pdf?ts=1707143795904&ref_url=https%253A%252F%252Fwww.google.com%252F

Use:

S2PI decoder;</br>
decoder.begin([serial_pin], [reset_pin]);

or

S2PI decoder([serial_pin], [reset pin]

To write to the device:

decoder.output([device_address (pin programmed, ref. datasheet)], [8 bit data]);

To reset the device (optional, reset's all pins, ref. datasheet):

decoder.reset();
