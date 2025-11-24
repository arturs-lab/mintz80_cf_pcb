# mintz80_cf_pcb
MintZ80 Compact Flash PCB

# releases
* [Rev 1](REV1.md)
* [Rev 1a](REV1a.md)
* [Rev 2](REV2.md)

# Jumper functions
* SJ1,SJ2 - select address range for the board. Either 0x40-0x7f or 0x80-0xaf
* SJ3 - selects clock for the YMZ sound chip. Either sysclock or TTL generator/active oscillator depending on which is populated. Do not populate both.
* SJ4,SJ5 - select addresses for CF card. Either 0x80 for CS0 and 0x88 for CS1 or 0x90 and 0x98 correspondingly. Do the math for when 0x40-0x7f range is selected.
* CFRST selects whether CF RESET pin is connected to system RESET line or to one of the ports for software-controlled reset. Unfortunately, trying to do software reset using CS1 ports does not seem to be working. Hence this hack.