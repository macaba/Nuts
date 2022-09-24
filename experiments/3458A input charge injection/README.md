# 3458A input charge injection

![Setup](images/Setup.jpg)

Keithley 428 (K428) current amplifier input wired to 3458A input, 1E06 V/A range. K428 output connected to MSO5074. 3458A on 10V range.

K428 voltage bias swept from -5V to 5V to observe change in charge injection.

There is a charge injection pulse at the start and end of the AZ period. I have made the assumption that they mark the beginning/end of the AZ period, rather than the input measurement period, because of the spacing of the pulses. For a 10 NPLC configuration, there are pulses at 0PLC (large), 10PLC (small), 21PLC (large), 31PLC (small). Note the additional 1PLC that is the meter waiting for the start of the next PLC before doing a new acquisition, it is my opinion that it is more likely the meter idles in the input measurement phase rather than the AZ phase so I am confident in labelling the larger pulses as "AZ period start". This is shown graphically in the 1 NPLC section.

## 1 NPLC

This shows the pulse train at 1NPLC

![Pulses](images/1NPLC.png)

## AZ period start

![LargePulse](images/Large%20pulse/Large_pulse.gif)

Peak-peak value range from 1.42uApp to 2.16uApp.

## AZ period end

![LargePulse](images/Small%20pulse/Small_pulse.gif)

Peak-peak value range from 0.60uApp to 1.08uApp.

