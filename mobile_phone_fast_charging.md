# Mobile phone battery and charging

* Generally contain Lethium ion battery.
  + Capacity measured in Ah (i.e. Ampere-Hour)
  + Min V: 3.0V
  + Average V: 3.7V - 3.8V
  + Max V: 4.2V

* Battery Pins
  1. GND (Battery negative terminal)
  2. BAT+ (Battery positive terminal)
  3. BTemp (Battery Temperature)
  4. BSI (Battery System Indicator)

* Charging circuit
  1. Direct Charger
  2. Switching Charger
  3. Direct Charger Divide/2
* Charger adaptor
  + SDP (Standard Downstream port)
    + 0.5A
  + CDP (Downstream port)
    + Upto 1.5A
  + DCP (Dedicatet charger port) 5V 1.5A
    + Data wire (D+, D-) are connected.
  + Samsung AFC
  + Qualcomm Quick-charge
    + QC 2.0
    + QC 3.0
  + USB Type-C PD (USB Power Deliver)
    + Power delivery along with data over a single cable.
    + Type:
      + USB Type-C: 5V @ 3A
      + USB Type-C PD: 5V, 9V, 15V, 20V (fixed)
      + USB Type-C PD & PPS: 3.3V - 21V (variable)
        + PPS: Programable Power Supply
    + It uses cc1 and cc2 to communicate about power delivery.

* USB cable
  + cable id ic: Tells the adaptor about how much current the cable can handle.

