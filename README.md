# Astérix: The Gallic War
Following requirements have to be met:
1. Game must be installed in the default path: `C:\Program Files (x86)\Infogrames\Asterix`
2. The `ASTERIX\Music` folder must be copied into the installation folder (`C:\Program Files (x86)\Infogrames\Asterix\Music`)
3. Overwrite the `Asterix.exe` with the one in this repository
4. (optional) Install dgVoodoo2 to run the game on modern hardware

Tested using English (US?) version of `Asterix.exe`. SHA256: `086F93E44B8424A69D69804AF4676CF86B75A7972676E2DA482293ED124B6080`.

## Notes
* the game loops through the drives skipping the `C` drive
* for each drive it checks `{DRIVE_LETTER}:\\Asterix\\Music\\T5_Carn.wav`
  * file must exist
  * file must NOT be writeable

Hexdump of patches:
```
0x00061fbf 02
0x00062014 9090
0x0014569d 43
0x001456a0 50726f67
0x001456a5 616d2046696c65732028783836295c496e666f6772616d65735c417374657269785c4d757369635c54355f4361726e2e77617600
```
