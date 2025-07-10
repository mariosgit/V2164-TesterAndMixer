# V2164 Tester / Mixer

Simple board to test V2164 chips. Follows the application example in the SSM2164 datasheet.

Can also be used as a 2 channel stereo mixer.

![](./images/Screenshot%202025-07-10%20at%2016.52.10.png)

## Status

Not tested yet. But looks nice.

### Gimmics

For cleverness sake, chip adapters can be used.

With R1/R4 and R14/R15 the range of the pots can be limited.
In theory 0V is 0dB and then the gain factor is -33mV/dB with a max range of -120..+20 dB, that means -0.66V=20dB and 3.96V=-120dB.

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

### Schematic

![](./images/Screenshot%202025-07-10%20at%2016.51.17.png)

