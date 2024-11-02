# Appendix E: Example USB Descriptors for HID Class Devices

- This appendix contains a sample set of descriptors for an imaginary product

> ##### Caution
>
> - This sample is intended for use as an instructional tool.
>
> - Do NOT copy this information verbatim -- even if building a similar device.
>
> - It is important to understand the function of every field in every descriptor and why each value was chosen.

- The sample device is a low-speed 105-key keyboard with an integrated pointing device.

- This device could be built using just one interface.

- However, two are used in this example so the device can support the boot protocol.

- As a result there are two Interface, Endpoint, HID and Report descriptors for this device.

## E.1 Device Descriptor

|Part|Offset/Size (Bytes)|Description|Sample Value|
|-|-|-|-|
|*idVendor*|8/2|Vendor ID (assigned by USB).|0xFFFF|
|*idProduct|10/2|Product ID (assigned by manufacturer).|0x0001|

## E.2 Configuration Descriptor

|Part|Offset/Size (Bytes)|Description|Sample Value|
|-|-|-|-|
|MaxPower|8/1|Maximum power consumption of USB device from bus in this specific configuration when the device is fully operational. Expressed in 2 mA units. The number chosen for this example is arbitrary|0x32|

## E.11 String Descriptors

|Part|Offset/Size (Bytes)|Description|Sample Value|
|-|-|-|-|
|*bLength*|00/01|Length of String descriptor in bytes.|0x04|
|*bDescriptorType*|01/01|Descriptor Type = String|0x03|
|*bString*|02/02|Array of LangID codes (in this case the 2-byte code for English).|0x0009|
|*bLength*|04/01|Length of String desscriptor.|0x0A|
|*bDescriptorType*|05/01|Descriptor Type = String|0x03|
|*bString*|06/08|Manufacturer|ACME|
|*bLength*|14/01|Length of String descriptor.|0x22|
|*bDescriptorType*|15/01|Descriptor Type = String|0x03|
|*bString*|16/32|Product Locator Keyboard|Locator Keyboard|
|*bLength*|48/01|Length of String descriptor.|0x0E|
|*bLength*|49/01|Descriptor Type = String|0x03|
|*bString*|50/12|Device Serial Number|ABC123|