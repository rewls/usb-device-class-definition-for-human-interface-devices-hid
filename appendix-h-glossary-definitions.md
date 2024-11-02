# Appendix H: Glossary Definitions

- This appendix defines terms used throughout this document.

- For additional terms that pertain to the USB, see Chapter 2, "Terms and Abbreviations," in the USB Specification.

## Array

- A series of data fields each containing an index that corresponds to an activated control.

- Banks of buttons or keys are reported in array items.

## Boot Device

- A device which can be used by host system firmware to assist in system configuration prior to the loading of operating system software.

- A non-boot device does not need to be functional until the operating system has loaded.

## Button bitmap

- A series of 1-bit fields, each representing the on/off state of a button.

- Buttons can be reported in either an array or a button bitmap.

## Class

- A USB device is organized into classifications such as **HID**, audio, or other-based on the device's features, supported requests, and data protocol.

## Collection

- A collection is meaningful grouping of **Input**, **Output**, and **Feature** items -- for example, mouse, keyboard, joystick, and pointer.

- A pointer **Collection** contains items for x and y position data and button data.

- The **Collection** and **End Collection** items are used to delineate collection.

## Control

- A sink or source of a data field -- for example, an LED is a sink or destination for data.

- A button is an example of a source of data.

## Control pipe

- The default pipe used for bi-directional communication of data as well as for device requests.

## Data phrase

- Part of a device's response to a request.

## Descriptor

- Information about a USB device is stored in segments of its ROM (read-only memory).

- These segments are called descriptors.

## Device class

- A method of organizing common functions and protocols for devices that serve similar functions -- for example, communication, audio, display, and so on.

## Device descriptor

- Packet of information that describes the device -- for example, the vendor, product ID, firmware version, and so on.

## Endpoint descriptor

- Standard USB descriptor describing the type and capabilities of a USB communication channel, or pipe.

## Feature control

- Feature controls affect the behavior of the device or report the state of the device.

- Unlike input or output data, feature data is intended for use by device configuration utilities and not applications.

- For example, the value for the repeat rate of a particular key could be a feature control.

- HID feature controls are unrelated to features discussed in Chapter 9 of the USB Specification.

## Feature item

- Adds data fields to a Feature report.

## Field

- A discrete section of data within a report.

## Frame

- A smallest unit of time on the Universal Serial Bus (USB); equal to 1 millisecond.

## HID (Human Interface Device)

- A cronym specifying either a specific class of devices or the type of device known as Human Interface Devices (HID) or HID class devices -- for example, a data glove.

- In this document, "HID class" is synonymous with a device of type: human interface.

## HID class

- This classification of USB devices associated with human interface devices (HID).

## HID class device

- A device of type: human interface and classified as such.

## HID descriptor

- Information about a USB device is stored in segments of its ROM (read-only memory).

- These segments are called descriptors.

## Host

- A computer with a USB port, as opposed to a device plugged into it.

## Hub

- A USB device containing one or more USB ports.

## Idle rate

- The frequency at which a device reports when no new events have occurred.

- Most devices only report new events and therefore default to idle rate of infinity.

- Keyboards may use the idle rate for auto repeating keys.

## Input item

- Adds one or more data fields to an input report.

- Input controls are a source of data intended for applications -- for example, x and y data.

## Interface descriptor

- The class field of this descriptor defines this device as a HID class device.

## Interrupt In pipe

- The pipe used to transfer unrequested data from the device to the host.

## Interrupt Out pipe

- The pipe used to transfer low latency data from the host to the device.

## Item

- A component of a Report descriptor that represents a piece of information about the device.

- The first part of an item, called the item tag, identifies the kind of information an item provides.

- Also, referred to generically as Report items.

<br>

- Included are three categories of items: Main, Global, and Local.

- Each type of item is defined by its tag.

- Also referred to as Main item tag, Global item tag, and Local item tag.

## Item parser

- The part of the HID class driver that reads and interprets the items in the Report descriptor.

## Logical units

- The value the device returns for Logical Minimum and Logical Maximum.

- See Physical units.

## LSB

- Least Significant Byte

## Main item

- An item that adds fields to a report.

- For example, Input, Output, and Feature items are all data.

## Message pipe

- Another name for the Control pipe.

## NAK

- The value returned when a request has been sent to the device and the device is not prepared to respond.

## Nibble

- A half of a byte; 4 bits.

## Non-USB aware

- An operating system, program loader, or boot subsystem which does not support USB per the core and device specifications.

- Examples include PC-AT BIOS and IEEE 1275 boot firmware.

## Null

- No value, or zero, depending upon context.

## Output item

- Adds one ore more data fields to an output report.

- Output controls are a destination for data from applications -- for example, LEDs.

## Packets

- A USB unit of information: Multiple packets make up a transaction, multiple transactions make up a transfer report.

## Part

- Document convention used to define bit attributes.

## Physical Descriptor

- Determines which body part is used for a control or collection.

- Each Physical descriptor consists of the following three fields: Designator, Qualifier and Effort.

## Physical units

- The logical value with a unit parameter applied to it.

- See Logical units.

## Pipes

- Pipes are different ways of transmitting data between a driver and a device.

- There are different types of pipes depending on the type of encoding or requesting that you want to do.

- For example, all devices have Control pipe by default.

- The Control pipe is used for message-type data.

- A device may have one or more Interrupt pipes.

- An Interrupt In pipe is used for stream-type data from the device and n optional Interrupt Out pipe may be used for low latency data to the device.

- Other types of pipes include Bulk and Isochronous.

- These two types of pipes are not used by HID class devices and are therefore not defined for use within this specification.

## Protocol

- A report structure other than the structure defined by the report descriptor.

- Protocols are used by keyboards and mice to insure BIOS support.

## Report

- A data structure returned by the device to the host (or vice versa).

- Some devices may have multiple report structures, each representing only a few items.

- For example, a keyboard with an integrated pointing device could report key data independently of pointing data on the same endpoint.

## Report descriptor

- Specifies fields of data transferred between a device and a driver.

## Set

- A group of descriptors -- for example, a descriptor set.

## Stream pipe

- Isochronous pipe used to transmit data.

## String descriptor

- A table of text used by one or more descriptors.

## Tag

- Part of a Report descriptor that supplies information about the item, such as its usage.

## Transaction

- A device may send or receive a transaction every USB frame (1 millisecond).

- When the item parser within the HID class driver locates a terminating item, the contents of the item state table are moved.

## Transfer

- One or more transactions creating a set of data that is meaningful to the device -- for example, Input, Output, and Feature reports.

- In this document, a transfer is synonymous with a report.

## Unknown Usage

- Unknown usages can be standard HID usages that an application predates or vendor defined usages not recognized by a generic application.

## Usage

- What items are actually measuring as well as the vendor's suggested use for specific items.

## USB Boot Device

- Device is USB HID "Boot/Legacy" compliant and Reports its ability to use the boot protocol, or report format, defined in the HID class specification for input devices such as keyboards or mouse devices.

## Variable

- A data field containing a ranged value for a specific control.

- Any control reporting more than on/off needs to use a variable item.

## Vendor

- Device manufacturer.
