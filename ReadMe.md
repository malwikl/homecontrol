```
rule1
on zbreceived#ZBButton4#cluster==10 do break 
on zbreceived#ZBButton4#endpoint=1 do  ZbSend {"device":"0x772D","send":{"Power":"Toggle"}} endon
on zbreceived#ZBButton4#endpoint=2 do  ZbSend {"device":"0x6699","send":{"Power":"Toggle"}} endon 
on zbreceived#ZBButton4#endpoint=3 do  ZbSend {"device":"0xD994","send":{"Power":"Toggle"}} endon
```

alternativ

```
Rule1 1
Rule1
  ON ZbReceived#ZBButton4#LidlPower DO Var4 %value% ENDON
  ON ZbReceived#ZBButton4#Endpoint DO Event Button%value%Clicked=%var4% ENDON
  ON Event#Button1Clicked=0 DO [Any_command_for_button1_clicked_once] ENDON
  ON Event#Button1Clicked=1 DO [Any_command_for_button1_clicked_twice] ENDON
  ON Event#Button2Clicked=0 DO [Any_command_for_button2_clicked_once] ENDON
  ON Event#Button2Clicked=1 DO [Any_command_for_button2_clicked_twice] ENDON
  ...
```
