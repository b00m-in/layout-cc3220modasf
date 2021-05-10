## [Contents](#contents)

Original CC3220MODASF footprint downloaded from Ultralibrarian.

see ~/dev/kicad/cc3220s/wifi_module/ul_CC3220MODASF12MONR/ (pls ignore - this is a local path) for original CC3220MODASF footprint. Some border lines and through holes in the middle thermal ground pads had to be removed and replaced with vias on the board. 

P.Cu is in fact a ground plane and G.Cu is a power plane

The order of the interface jumpers has changed between CC3220S-LAUNCHXL and LAUNCH-CC3220MODASF. On the former VCC_BRD and VBATT_CC could be jumped as they were next to one another. 

Also J9 came jumped on the former so U7 (op-amp in adc circuit) was powered by VCC_BRD but it's not jumped by default on the latter - didn't catch that as the adc functionality hasn't been yet tested on the latter.  


TMP006AIYZFR is obsolete so was replaced by TMP116NAIDRVR 


## [Layout](#layout)

The following GPIO ports were left unconnected due to space constraints on board:
```
P05_GPIO_14
P06_GPIO_15
P07_GPIO_16
P08_GPIO_17
P18_GPIO_28
P45_GPIO_31 / DCDC_ANA2_SW_P - not connected on dev board either
DCDC_ANA2_SW_N (P46) 
```

CC3220S/F <-> CC3220MODAS
```
Pin55 GPIO1 UART0_TX <-> Pin46
Pin57 GPIO2 UART0_RX <-> Pin47

Pin07 GPIO16 UART1_TX <-> Pin07
Pin08 GPIO17 UART1_RX <-> Pin08
```
~/ti/ccsv8/simplelink_cc32xx_sdk_3_10_00_04/source/ti/boards/CC3220S_LAUNCHXL/CC3220S_LAUNCHXL.c
.rxPin = UARTCC32XX_PIN_08_UART1_RX --> .rxPin = UARTCC32XX_PIN_45_UART1_RX



### [References](#references)
+ [](https://)
+ [](https://) 
+ [](https://)

