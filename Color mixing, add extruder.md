pins.h 

# disable configuration_adv.h
```
//#define LIN_ADVANCE
```


# increase thermal protection

```
#if ENABLED(THERMAL_PROTECTION_HOTENDS)
  #define THERMAL_PROTECTION_PERIOD 120 

  #define WATCH_TEMP_PERIOD 60                // Seconds
  #define WATCH_TEMP_INCREASE 2               // Degrees Celsius
```

# disable in configuration.h
```

//#define SINGLENOZZLE

//#define SINGLENOZZLE  // Enable this if you are using a single mixing nozzle (requires DUAL_EXTRUDER)
//#define DUAL_EXTRUDER // If not single nozzle, primary nozzle plugged in to E0 port
```

## Change extruders to:
```
#if ENABLED(DUAL_EXTRUDER)
   #define EXTRUDERS 2
   #define EXTRUDERS 3
#else
   #define EXTRUDERS 1
   #define EXTRUDERS 3
#endif
```

# enable mixing:
```
#define MIXING_EXTRUDER
#if ENABLED(MIXING_EXTRUDER)
  #define MIXING_STEPPERS 3        // Number of steppers in your mixing extruder
  #define MIXING_VIRTUAL_TOOLS 16  // Use the Virtual Tool method with M163 and M164
  //#define DIRECT_MIXING_IN_G1    // Allow ABCDHI mix factors in G1 movement commands
#endif
```

# pins_ramps.h add third extruder:
```
//addred on 29-09-2018
//#define X_MAX_PIN         2
//#define Z_MAX_PIN          19
//#define Y_MAX_PIN          15

#define E2_STEP_PIN        2
#define E2_DIR_PIN         15
#define E2_ENABLE_PIN      19
```
# disable old pins
```
#define X_MAX_PIN         -1
#define Z_MAX_PIN          -1
#define Y_MAX_PIN          -1
```
