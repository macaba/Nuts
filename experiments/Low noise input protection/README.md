# Low noise input protection

When trying to protect noise sensitive inputs (like nanovolt amplifiers), it can be tricky to protect against continuous voltage without introducing noise (e.g. from a 50k input resistor). GDT + MOV remain suitable for protection against ESD.

![Schematic](images/Schematic.png)

In this protection circuit, a JFET is used as a constant current limiter. Leakage through D2 to the JFET ensures proper operation. D3 clamps the output voltage. The maximum protection voltage is limited by the rating of the JFET (25V in this case) and careful selection of the JFET is required to not introduce additional noise.

Behaviour:
10V input = 24mA current, 0.87V on output.
25V input = 33mA current, 0.88V on output.

10V input JFET temperature:

![Schematic](images/10V input.png)

25V input JFET temperature:

![Schematic](images/25V input.png)
