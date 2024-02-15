# SN74LV8153
Arduino UNO library for Serial to Parallel Interface SN74LV8153 chip
ref. datasheet: https://www.ti.com/lit/ds/symlink/sn74lv8153.pdf?ts=1707143795904&ref_url=https%253A%252F%252Fwww.google.com%252F

<u>Use:</u>

S2PI decoder;</br>
decoder.begin([serial_pin], [reset_pin]);

or

S2PI decoder([serial_pin], [reset pin]

<u>To write to the device:</u>

decoder.output([device_address (pin programmed, ref. datasheet)], [8 bit data]);

<u>To reset the device (optional, reset's all pins, ref. datasheet):</u>

decoder.reset();
