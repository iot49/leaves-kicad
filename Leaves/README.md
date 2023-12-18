# Leaves

## Leaf 01: FRAM, Gyro, Canbus, BMI270, Hall Current Sensors (ADS1015), Supply Voltage Sense

* FRAM
* Canbus
* INA3221     
  * BUG: IN1-, IN2- not connected - Vsense1, Vsense2 always zero
  * Channel3 works (Vbus = Vin = ~12V nominal)
* ADS1015
* BMI270
* TMP1075     
  * BUG: address conflict with ADS1015 (TMP1075 removed)

## Leaf 02: FRAM, Gyro, Canbus, BMI270, Hall Current Sensors (ADS1015), Voltage Sense, Temperature

* Leaf 01 fixed
  * TMP1075 at 0x49
  * INA3221: IN1-=IN1+, IN2-=IN2+

## Leaf 03: Hall Current Sensors (ADS1015), Voltage Sense, Temperature, Buses (???)

* Leaf 01/02 with different buses
  * no Canbus, Gyro

* 3 (or 4) Hall Current Sensors
* Switched 12V (2 simultaneously should suffice)
  * Fan
  * Battery low voltage disconnect Victron BP12/24-100
  * House to Chassis charger
* 3 voltage inputs
  * Ignition
  * Chassis battery voltage
  * BP12 disconnect. Note: Power Leaf from an unswitched source, e.g. chassis

Connectors:  (Hammond 1593VBK accommodates up to 93mm)
* 4 Hall         40   mm
* 1 fan          10   mm
* Tool free: 8   33   mm  (3.5mm, 16-24 gauge)
  * 2 for Power, Ground
  * 3 Voltage inputs
  * 2 Switched outputs (1 shared with fan?)
  * 1 extra?
* Extra grove connectors other side? 3/5V?
* Buses fro Trume, Xantrex, RVC, Linbus?

Maybe:

* Bus for
  * Truma water heater
  * Xantex freedom 2000
  * Dometic fridge (Linbus)

## Leaf 04: Cooling Fan Controller, 12V switched out