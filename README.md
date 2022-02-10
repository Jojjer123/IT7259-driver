# How to use

## Necessary initialization
In setup():
```
Wire.begin();
delay(1000);
```
Delay added to ignore odd readings from the capacitive touch panel directly after startup, which might not be the case for you.


### Get the device name
```
char myDeviceName[7];
getDeviceName(myDeviceName);
```


### Get capabilities of the device
```
struct PanelCapabilities myPanelCap;
getPanelCapabilities(&myPanelCap);
```


### Set interrupt notification behaviour
```
setInterruptNotificationBehaviour(a, b);
```
The variable ***a*** can take the form of:  
* 0 - Disabled
* 1 - Enabled
And the variable ***b*** can take the form of:  
* 0 - Low level trigger
* 1 - High level trigger
* 2 - Falling edge trigger
* 3 - Rising edge trigger


### Set the power mode to idle
```
setPowerModeIdle();
```



### Reset the event queue
```
resetEventQueue();
```




### Resets the firmware
```
resetFirmware();
```



### Sets the charge mode
```
setChargeMode(true);
```
Can be set to true or false:  
* true - Enter charge mode
* false - Enter normal mode



### Sets the GSM mode
```
setGsmMode(true);
```
Can be set to true or false:  
* true - Enter GSM mode
* false - Exit GSM mode



### Get the cdc tune level of the algorithm
```
uint16_t cdcTuneLevel;
getAlgorithmParam(&cdcTuneLevel);
```
