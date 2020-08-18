# aMpeX Klipper Macros

These macros are offered mostly as a starting place. 
Please read them, and understand what they are doing, before blindly copying them into your own configuration.

## test
| File | Macro | Description | Notes |
|---|---|---|---|
| macros_fan.cfg | PIN_FAN_SPEED | a macro to fix the part fan speed, overriding the speeds from the slicer | Works in conjuction with the modified M106 and M106 in the same file |
| macros_fan.cfg | M106 | A modified M106, to be used with the PIN_FAN_SPEED macro | |
| macros_fan.cfg | M107 | A modified M107, to be used with the PIN_FAN_SPEED macro | |
| macros_filament.cfg | unload_filament | a filament unloader| Modify G0 E-900 F2400 to fit your unload distance.Note that your screen will not use the macro without additional changes |
| macros_filament.cfg | load_filament | a filament loader | Modify G0 E800 F2400 to fit your load distance. Note that your screen will not use this macro without additional changes  |
| macros_filament.cfg | preheat_abs | a simple preheat | |
| macros_pressure_advance.cfg | M900 | a simple mapping of M900 to SET_PRESSURE_ADVANCE | |
| macros_pressure_advance.cfg | SELECT_PA | A macro which creates a lookup table for pressure advance, based on Filament and Nozzle | you will need to replace variable_pa_* with your own filaments, nozzles, and p.a. sizes following the format seen in the macro |
