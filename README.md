## [Contents](#contents){#contents}




 

see ~/dev/kicad/cc3220s/wifi_module/ul_CC3220MODASF12MONR/ for original CC3220MODASF footprint. Some border lines and through holes in the middle thermal ground pads had to be removed and replaced with vias on the board. 

P.Cu is in fact a ground plane and G.Cu is a power plane


The order of the interface jumpers has changed between CC3220S-LAUNCHXL and LAUNCH-CC3220MODASF. On the former VCC_BRD and VBATT_CC could be jumped as they were next to one another. 

Also J9 came jumped on the former so U7 (op-amp in adc circuit) was powered by VCC_BRD but it's not jumped by default on the latter - didn't catch that as the adc functionality hasn't been yet tested on the latter.  




TMP006AIYZFR is obsolete so was replaced by TMP116NAIDRVR 




### [References](#references){#references}
+ [](https://)
+ [](https://) 
+ [](https://)

