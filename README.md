# V2164 Tester / Mixer

Simple board to test V2164 chips. Follows the application example in the SSM2164 datasheet.

Can also be used as a 2 channel stereo mixer.

![](./images/Screenshot%202025-07-10%20at%2016.52.10.png)

## Status

Not tested yet. But looks nice.

### Gimmics

For cleverness sake, chip adapters can be used.

With R1/R4 and R14/R15 the range of the pots can be limited.  **For testing u can just short the**.
In theory 0V is 0dB and then the gain factor is -33mV/dB with a max range of -120..+20 dB, that means -0.66V=+20dB and 3.96V=-120dB.

Ask yor favorite chat bot for a volage divider fitting your needs.

    To design a voltage divider with three resistors in series between +12V and -12V that meets your specified voltage requirements, we'll follow these steps:

    ### Given:
    - **Supply voltages**: +12V (top) and -12V (bottom)
    - **Middle resistor (R₂)**: 10 kΩ
    - **Desired voltage at top of R₂ (V₂)**: +3.96V
    - **Desired voltage at bottom of R₂ (V₃)**: -0.66V

    bla bla bla...

    ### Final Resistor Values:
    - **Top resistor (R₁)**: **17.4 kΩ**
    - **Middle resistor (R₂)**: **10 kΩ** (given)
    - **Bottom resistor (R₃)**: **24.55 kΩ**

    ### Practical Considerations:
    - You may need to use standard resistor values close to the calculated ones (e.g., 17.4 kΩ ≈ 17.8 kΩ or 18 kΩ; 24.55 kΩ ≈ 24.9 kΩ or 25 kΩ). 
    - For higher precision, you can use a potentiometer or combine resistors in series/parallel.

Or use the experimental [falstad circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgpABZsKBTAWjDACgA3WvEPKmnmGIooomlTAiq06Ak7dwwhdjSj+EqWtlsATiBQJCvKgaNgaNUWni79h-eLtGV05DYDuTkC-AXvqyDZPU2NfSz4oIIUhEXNLGMiABzDQuMURelcweBy2ZLSEtJ9M0WycuCii1QF-aUq-CJqIwOS6WKU270hLEolyirAMSxCi7ocJNzgoWRAAJQYAZwBLBYAXAEMAOwBjBjYAcxAWMyVj8bUD2hUuy07sBE1AzzOEmoSnm-Sr9qk87wfzvcMgDepNcq1iGY-DRIV5QWVylEYVDhvY0h8gecQihHBiQQC7mMPoTbrCQoEgA).

### BOM

| References | Value | Footprint | Quantity |
|---|---|---|---|
| C5, C6, C7, C8               | 560p | 603 | 4 |
| C2, C3                       | 220p (100p+) | 603 | 2 |
| R2, R3, R5, R6, R7, R8 | 33k | 603 | 6 |
| R10, R11, R12, R13, R16, R17 | 470 | 0603 | 6 |
| R1, R4, R14, R15             | 5k see notes | 603 | 4 |
| *R9*                         | 7.5k for class A or *open for class AB* | 603 | 1 |
| U1                           | SSI2164 | DIP-16 7.62mm or SO-16 + Adapter | 1 |
| U2                           | TL074 | DIP-14 7.62mm or SO/SOP/TSOP-14 + Adapter | 1 |
| RV1, RV2                     | 10k see notes | 9mm Potentiometer Vertical | 2 |


### Schematic

![](./images/Screenshot%202025-07-10%20at%2016.51.17.png)

### Reference from DS

![](./images/Screenshot%202025-07-10%20at%2016.49.57.png)

Also read the datasheet, just search for "V2164 pdf" or "SSM2164 pdf".