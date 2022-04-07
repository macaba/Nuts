# Nuts

An assortment of data and observations regarding electronics metrology and precision analog electronics

## ADR1399 output voltage deviation vs. heater voltage

The ADR1399 datasheet discusses the improved output dynamic impedance for reducing the change of output voltage vs. zener supply current. What about the heater supply voltage?

With heater+ at 15V, and heater- swept from 0V to -15V (to give 15-30V heater voltage range), output voltage coefficient is 0.37 ppm/V. Heater+ is fixed at 15V as this also supplies the zener current (through 2.35k Rshunt).

![ADR1399](images/ADR1399%20output%20voltage%20deviation%20vs%20heater%20voltage.png)

## VRE102CA voltage reference noise from batch of 8

Powered from +/-14V supply, with positive reference output going into 0.1 - 10Hz LNA.

![VRE102CA](images/VRE102CA.png)

## MOSFET Idss leakage with 0V gate at 21°C

Using Keithley 617 electrometer, with +/-100V DAC output, to sweep the drain pin of MOSFETs from 0.1V to maxV, gate pin and source pin shorted together (and wired into electrometer input).

![Leakage](images/MOSFET%20leakage.png)
