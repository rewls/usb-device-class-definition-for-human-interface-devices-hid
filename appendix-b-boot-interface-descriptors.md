# Appendix B: Boot Interface Descriptors

- The HID Subclass 1 defines two descriptors for Boot Devices.

- Devices may append additional data to these boot reports, but the first 8 bytes of keyboard reports and the first 3 bytes of mouse reports must conform to the format defined by the Boot Report descriptor in order for the data to be currently interpreted by the BIOS.

- The report may not exceed 8 bytes in length.

- The BIOS will ignore any extensions to reports.

- These descriptors describe reports that the BIOS expects to see.

- However, since the BIOS does not actually read the Report descriptors, these descriptors do not have to be hard-coded into the device if an alternative report descriptor is provided.

- Instead, descriptors that describe the device reports in a USB-aware operating system should be included (these may or may not be the same).

- When the HID class driver is loaded, it will issue a Change Protocol, changing from the boot protocol to the report protocol after reading the boot interface's Report descriptor.

## B.1 Protocol 1 (Keyboard)

- The following represents a Report descriptor for a boot interface for a keyboard.

    ```
    Usage Page (Generic Desktop),
    Usage (Keyboard),
    Collection (Application),
        Report Size (1),
        Report Count (8),
        Usage Page (Key Codes),
        Usage Minimum (224),
        Usage Maximum (231),
        Logical Minimum (0),
        Logical Maximum (1),
        Input (Data, Variable, Absolute),   ; Modifier byte
        Report Count (1),
        Report Size (8),
        Input (Constant),                   ; Reserved byte
        Report Count (6),
        Report Size (8),
        Logical Minimum (0),
        Logical Maximum (255),
        Usage Page (Key Codes),
        Usage Minimum (0),
        Usage Maximum (255),
        Input (Data, Array),
    End Collection
    ```

- The following table represents the keyboard input report (8 bytes).

    |Byte|Description|
    |-|-|
    |0|Modifier keys|
    |1|Reserved|
    |2|Keycode 1|
    |3|Keycode 2|
    |4|Keycode 3|
    |5|Keycode 4|
    |6|Keycode 5|
    |7|Keycode 6|

> ##### Note
>
> - Byte 1 of this report is a constant.
>
> - This byte is reserved for OEM use.
>
> - The BIOS should ignore this field if it is not used.
>
> - Returning zeros in unused fields is recommended.
