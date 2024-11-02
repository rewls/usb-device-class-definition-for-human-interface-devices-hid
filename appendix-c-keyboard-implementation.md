# Appendix C: Keyboard Implementation

- The following are the design requirements for USB keyboards:

    - Non-modifier keys must be reported in Input (Array, Absolute items.

        - Reports must contain a list of keys currently pressed and not make/break codes (relative data).

    - The order of keycodes in array fields has no significance.

        - Order determination is done by the host software comparing the contents of the previous report to the current report.

        - If two or more keys are reported in one report, their order is indterminate.

        - Keyboards may buffer events that would have otherwise resulted in multiple event in a single report.

    - "Repeat Rate" and "Delay Before First Repeat" are implemented by the host and not in the keyboard (this means the BIOS in lagacy mode).

        - The host may use the device report rate and the number of reports to determine how long a key is being held down.

        - Alternatively, the host may use its own clock or the idle request for the timing of these features.

    - For Boot Keyboards, the reported index for a given key must be the same values as the key usage for that key.

        - This is required because the BIOS will not read the Report descriptor.

        - It is recommended (but not required) that non-legacy protocols also try to maintain a one-to-one correspondence between indices and Usage Tags where possible.

    - Boot Keyboards must support the boot protocol and the Set_Protocol request.

        - Boot Keyboards may support an alternative protocol (specified in the Report descriptor) for use in USB-aware operating environments.
