# Directed
Acoustic beamforming and beamsteering. Accenture Industry X LabDays 2023 Project.

Inspired by:
- [Student project at Cornell](https://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/s2012/tcj26_ecs227/tcj26_ecs227/index.html)
- [Charles Grassin's pretty much the same project](https://charleslabs.fr/en/project-Acoustic+beamsteering+with+a+speaker+array)

## Materials
- [Audio Waves](https://openstax.org/books/university-physics-volume-1/pages/17-2-speed-of-sound)

## Basic idea

We are going to play sound at 8 speakers simultaneously. Due to wave effects the sound will be amplified at normal direction and diminished to the sides.

## Planning

### Hardware

There are 2 variants of hardware and we don't know yet which one turns out better:

1. MCU [SPI] -- External DAC -- Amplifier -- Speaker
2. MCU [I2S] -- AudioDecoder [3.5mm jack] -- Amplifier -- Speaker

That leads us to a list of purchases:

| ECU                                    | Why needed                                       | Amount |
|----------------------------------------|--------------------------------------------------|--------|
| STM32F4Discovery                       | Main MCU, STM32F407VG: 2 12-bit DAC, 2 I2S, SDIO | 1      |
| Adafruit MicroSD card reader           | MicroSD card reader, that can be used by an MCU  | 1      |
| INTENSO MSDHC4G                        | MicroSD card 4Gb                                 | 1      |
| LM386 breakout board                   | Audio amplifier, from 4 Ohm, 0.325               | 8      |
| VIS K23-8                              | Speaker, 8 Ohm, 0.3W, up to 20kHz                | 8      |
| Adafruit I2S Stereo Decoder - UDA1334A | I2S to 3.5mm jack                                | 4      |
| BOOST-DAC8568                          | External 8 channel DAC                           | 1      |
| DELOCK 65419                           | 3.5mm plug with clamps                           | 4      |

Tools:
- Oscilloscope
- Multimeter
- Soldering iron
- Wires
- Breadboards
- Power module

### Modeling

- [ ] Formulas for sound processing
- [ ] Distance between speakers
- [ ] Criteria of efficiency for the multiple frequency case

### Hardware testing

Snippet-like project to use the hardware before the actual project

### Software development

Links to learn embedded programming in general and STM32 in particular

- [Step by step](https://wiki.st.com/stm32mcu/wiki/STM32StepByStep:Getting_started_with_STM32_:_STM32_step_by_step)
- [Play WAV-file](https://controllerstech.com/waveplayer-using-stm32-discovery/)
- And there's plenty information in Google both on embedded and STM32
