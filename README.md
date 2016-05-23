# DieselTuningBox
Open source rail pressure tuning software for Diesel engines

Initial design is for the first and second generation Bosch diesel injection, mainly VW.

Design process and tips at www.hackcorrelation.com/search/label/diesel

Everything here is just a prototype and will not work out of the box.
No warranty offered, it may even break your test car or trigger unresettable errors.

Terminal commands:
- h - help: show available commands
- e - enable offset ('boost' car)
- d - disable offset (do nothing)
- rm - reads the minimum value from which the module starts working
- rM - reads the maximum range
- rc - outputs the entire configuration (version, min, max, curve points)
- sm - sets the minimum range. Example: input sm300 - press enter
- sM - sets the maximum range. Example: sM800
- sC - sets a point on the curve. E.g. sC5117 sets point five to value 117. This means that during that specific range the output will be offset above by 17%
- sX - sets the entire configuration in a single string. Can be generated by the spreadsheet
- S - saves the config to EEPROM
- L - loads the config from EEPROM, overwriting the current one

By default the module starts disabled, outputing the unmodified ADC input. See blog post for details, the input and output impedance still need some work as the car expect very specific values.
