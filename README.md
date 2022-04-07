# Nuts

An assortment of data and observations regarding electronics metrology and precision analog electronics

## ADR1399 output voltage deviation vs. heater voltage

The ADR1399 datasheet discusses the improved output dynamic impedance for reducing the change of output voltage vs. zener supply current. What about the heater supply voltage?

With heater+ at 15V, and heater- swept from 0V to -15V (to give 15-30V heater voltage range), output voltage coefficient is 0.37 ppm/V. Heater+ is fixed at 15V as this also supplies the zener current (through 2.35k Rshunt).

![ADR1399](images/ADR1399%20output%20voltage%20deviation%20vs%20heater%20voltage.png)

## ADR1399 output voltage noise vs. zener supply current

It is known that the internal schematic of LM399 means that as long as a minimum current condition is met, there should not be any change in output voltage noise for higher currents as the actual zener current is fixed. This is confirmation that the ADR1399 is the same. 1mA is below the allowable range of shunt current, it is shown here as a point of interest.

![ADR1399 noise](images/ADR1399%20output%20noise%20vs%20zener%20current.png)

## VRE102CA voltage reference noise from batch of 8

Powered from +/-14V supply, with positive reference output going into 0.1 - 10Hz LNA.

![VRE102CA](images/VRE102CA.png)

## Solartron 7081 warmup with 10V input, comparison of 2 firmwares

MickleT has provided a modified Solartron 7081 firmware which resolves an issue with post-mux switching dwell time, to allow internal circuits to settle before taking zero reading.

![S7081](images/S7081%20startup.png)

## MOSFET Idss leakage with 0V gate at 21°C

Using Keithley 617 electrometer, with +/-100V DAC output, to sweep the drain pin of MOSFETs from 0.1V to maxV, gate pin and source pin shorted together (and wired into electrometer input). FOM is (10V/(datasheet RDS at 10V))/(leakage at 10V) to provide a quick comparison point.

![Leakage](images/MOSFET%20leakage.png)
