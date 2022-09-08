## Pseudocode for external garage door keypad entry 

### Assumptions:
  - Opening function of a garage door can be operated remotely by a control panel.
  - Control panel has to be located near garage door on adjoining garage door jam.
  - Control panel is powered.
  - User has basic knowledge on how a garage keypad functions.
  - Main motor unit is powered.


### START: Create variables for the program
1. CONTROL PANEL = controlPanel
    - Device that communicates to main motor unit.

2. MAIN MOTOR UNIT = motorUnit
    - Motorized device that operates/pulls the door open.  


### FUNCTION:
 
```js
FUNCTION checkDoorStatus:
  IF door = open
    THEN
      Do not accept passcode
        END
  ELSE door = closed
    THEN
      Accept passcode
        END
        
FUNCTION checkControlPanel
  IF control panel = not paired or connected unit
    THEN
      END
  ELSE 
    control panel = paired to motor unit
      Accept passcode
        END
      
FUNCTION clearMemory
  IF wrong passcode is entered OR door has been opened
    THEN
      clear passcode from panel
        END

 FUNCTION checkPasscode:
  IF passcode entered = correct
    THEN
      open door and clear control panel memory     
  ELSE 
    passcode entered = wrong  
      THEN
        clear passcode from panel memory and alert user
          END
 ```
 
 
 ### START:
 ```
 checkDoorStatus
 checkControlPanel
 checkPasscode
 ```
 
 ### END:
 ```
 clearMemory
 ```
 
![image](https://user-images.githubusercontent.com/101759410/189179621-ff23df61-89fc-4b74-9b3e-10f0a6d956a6.png)
