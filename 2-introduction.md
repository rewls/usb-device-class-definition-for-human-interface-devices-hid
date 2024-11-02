# 2. Introduction

- Universal Serial Bus (USB) is a communications architecture that gives a personal computer (PC) the ability to interconnect a variety of devices using a simple four-wire cable.

- The USB is actually a two-wire serial communication link that runs at either 1.5 or 12 megabits per second (mbs).

- USB protocols can configure devices at startup or when they are plugged in at run time.

- These devices are broken into various device classes.

- Each device class defines the common behavior and protocols for devices that serve similar functions.

- Some examples of USB device classes are shown in the following table:

> |Device Class|Example Device|
> |-|-|
> |Display|Monitor|
> |Communication|Modem|
> |Audio|Speakers|
> |Mass storage|Hard drive|
> |Human interface|Data glove|

> ##### See Also
>
> - For more information on terms and terminology, see Appendix H: Glossary Definitions.
>
> - The rest of this document assumes you have read and understood the terminology defined in the glossary.

## 2.1 Scope

- This document describes the Human Interface Device (HID) class for use with Universal Serial Bus (USB).

- Concepts from the USB Specification are used but not explained in this document.

> ##### See Also
>
> - The USB Specification is recommended pre-reading for understanding the content of this document.
>
> - See Section 2.3: Related Documents.

- The **HID** class consists primarily of devices 

## 2.2 Purpose

- This document is intended to supplement the USB specification and provide HID manufacturers with the information necessary to build USB-compatible devices.

- The primary and underlying goals of the HID class definition are to:

    - Be as compact as possible to save device data space.

    - Allow the software application to skip unknown information.

    - Be extensible and robust.

    - Support nesting and collections

    - Be self-describing to allow generic software applications.

## 2.3 Related Documents

- This document references the following related documents:

    |Name|Comment|
    |-|-|
    |Universal Serial Bus (USB) Specification, Version 1.0|In particular, see Chapter 9, "USB Device Framework."|
    |USB Class Specification for Legacy Software||
    |USB HID Usage Supplement|A detailed extension of the usages listed in Appendix A.|
    |USB Physical Interface Device (PID) Specification|
    |USB Audio Device Class|
