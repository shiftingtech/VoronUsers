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
|macros_print_startstop.cfg | prime_nozzle | Moves to the corner and makes a line| Update the X & Y coordinates for your bed |
|macros_print_startstop.cfg | clean_nozzle | moves the nozzle rapidly back and forth through a wiper | update (120,319) & (60,319) to match the opposite sides of your brush.  Requires Macro move_to_wiper |
|macros_print_startstop.cfg | move_to_wiper | moves the nozzle into position to begin a wipe | update the X Y & Z coordinates to match your wiper. |
|macros_print_startstop.cfg | start_code | for use at the start of a print:  Heats,Homes, QGL's, wipes, and primes |  requires Macros: move_to_wiper, clean_nozzle, and prime_nozzle |
|macros_print_startstop.cfg | stop_gcode | for use at the end of a print: parks the toolhead, and optionally turns off the heaters | requires Macro: conditional_turn_off_heaters |
|macros_print_startstop.cfg | conditional_turn_off_heaters | for use in stop_gcode.  Tracks an option for whether or not to turn off the heaters | works in conjuction with Macro set_turn_off|
|macros_print_startstop.cfg | set_turn_off | sets whether or not conditional_turn_off_heaters should turn off the heaters | requires macro: conditional_turn_off_heaters
|macros_print_startstop.cfg | heatsoak | a heat soak macro, to ensure the printer has completely warmed up before heating.  Based on slowly moving the toolhead around the bed | the coordinates of all 5 G0 commands should be updated to match your printer |
