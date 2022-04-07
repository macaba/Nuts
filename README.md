# Nuts

An assortment of data and observations regarding electronics metrology and precision analog electronics.

[ADR1399 output voltage deviation vs. heater voltage](#adr1399heater)  
[ADR1399 output voltage noise vs. reference current](#adr1399referencecurrent)  
[VRE102CA voltage reference noise in batch of 8](#vre102ca)  
[LTZ1000 unheated TC](#ltz1000unheated)  
[Solartron 7081 warmup with 10V input, comparison of 2 firmwares](#s7081warmup)  
[Solartron 7081 linearity](#s7081inl)  
[Keithley DMM6500 linearity](#k6500inl)  
[Keithley DMM6500 leakage](#k6500leakage)  
[MOSFET Idss leakage with 0V gate at 21°C](#mosfetleakage)  
[OPA140 CMRR](#opa140cmrr)  
[LT3042 & LT3093 low frequency noise](#ldonoise)  
[G3VM-41GR6 SSR off-leakage](#ssrleakage)
<a name="adr1399heater"/>
## ADR1399 output voltage deviation vs. heater voltage

The ADR1399 datasheet discusses the improved output dynamic impedance for reducing the change of output voltage vs. zener supply current. What about the heater supply voltage?

With heater+ at 15V, and heater- swept from 0V to -15V (to give 15-30V heater voltage range), output voltage coefficient is 0.37 ppm/V. Heater+ is fixed at 15V as this also supplies the zener current (through 2.35k Rshunt).

![ADR1399](images/ADR1399%20output%20voltage%20deviation%20vs%20heater%20voltage.png)
<a name="adr1399referencecurrent"/>
## ADR1399 output voltage noise vs. reference current

It is known that the internal schematic of LM399 means that as long as a minimum current condition is met, there should not be any change in output voltage noise for higher currents as the actual zener current is fixed. This is confirmation that the ADR1399 is the same. 1mA is below the allowable range of reference current, it is shown here as a point of interest.

![ADR1399 noise](images/ADR1399%20output%20noise%20vs%20zener%20current.png)
<a name="vre102ca"/>
## VRE102CA voltage reference noise in batch of 8

Powered from +/-14V supply, with positive reference output going into 0.1 - 10Hz LNA.

![VRE102CA](images/VRE102CA.png)
<a name="ltz1000unheated"/>
## LTZ1000 unheated TC

Uncorrected TC of LTZ1000 = 33-37 PPM/C.
Corrected TC with 17 ohm resistor = around 0 PPM/C.

Top line in each series is the heat up (using internal heater), bottom line is the cool down.

![LTZ1000](images/LTZ1000%20unheated%20TC.png)
<a name="s7081warmup"/>
## Solartron 7081 warmup with 10V input, comparison of 2 firmwares

MickleT has provided a modified Solartron 7081 firmware which resolves an issue with post-mux switching dwell time, to allow internal circuits to settle before taking zero reading.

![S7081](images/S7081%20startup.png)
<a name="s7081inl"/>
## Solartron 7081 linearity

![S7081INL](images/S7081%20linearity.png)
<a name="k6500inl"/>
## Keithley DMM6500 linearity

DMM6500 set to 1NPLC, high impedance input, autozero enabled.
Per step; 80 seconds to allow the PWM DAC output to settle, approximately 1 minute of samples acquired and averaged to give a single value for the chart.

![K6500](images/DMM6500%20linearity.png)
<a name="k6500leakage"/>
## Keithley DMM6500 leakage

Connected a lead from the PE screw on the rear panel, to the current input, digitize mode with 100uA range. 140nApp. Lead is unplugged halfway through the trace.

![K6500](images/DMM6500%20PE%20leakage.png)
<a name="mosfetleakage"/>
## MOSFET Idss leakage with 0V gate at 21°C

Using Keithley 617 electrometer, with +/-100V DAC output, to sweep the drain pin of MOSFETs from 0.1V to maxV, gate pin and source pin shorted together and wired into electrometer input. FOM is (10V/(datasheet RDS at 10V))/(leakage at 10V) to provide a quick comparison point.

![Leakage](images/MOSFET%20leakage.png)
<a name="opa140cmrr"/>
## OPA140 CMRR

OPA140 configured as unity gain buffer. DMM measuring input-to-output. Measured CMRR = 142dB.

![Leakage](images/OPA140%20CMRR.png)
<a name="ldonoise"/>
## LT3042 & LT3093 low frequency noise
 
 22uF Cset. Datasheet hides the 0.1-10 Hz region for good reason...
 
![Leakage](images/LT%20LDO%20noise.png)
<a name="ssrleakage"/>
## G3VM-41GR6 SSR off-leakage

Using Keithley 617 electrometer, with +/-100V DAC output, to sweep a pin of the SSR from 0.1V to 40V. Other pin wired to electrometer input.

![SSR leakage](images/G3VM-41GR6%20off%20leakage.png)
