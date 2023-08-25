# Electric-Motor-Temperature---PROJECT-
Electric Motor Temperature - PROJECT 
## EDA
There are 998070 rows and 13 columns in the dataset. 
No Null Fields.
Outiers Observed in ambient , u_d , torque , i_q , pm independent Features.
High Correlation Between Independent Variables. This Could lead to problem with model’s performance due to multi-collinearity

The data set is collected from several sensors from permanent magnet synchronous motor deployed on test bench.

All recordings are sampled at 2 Hz. i.e 2 cycles / second.
The motor is excited by hand-designed driving cycles denoting a reference motor speed and a reference torque.
Currents in d/q-coordinates (columns "i_d" and i_q") and voltages in d/q-coordinates (columns "u_d" and "u_q") are a result of a standard control strategy trying to follow the reference speed and torque.
Columns "motor_speed" and "torque" are the resulting quantities achieved by that strategy, derived from set currents and voltages.
In permanent magnet synchronous motor the rotor contains permanent magnets, while the stator consists of windings that generate a rotating magnetic field when energized.

## Operational Terms
Field weakening operation in a Permanent Magnet Synchronous Motor (PMSM) refers to the control strategy used to operate the motor at speeds higher than its base or rated speed. The base speed is typically limited by the maximum voltage and current that can be supplied to the motor while maintaining the magnetic field within the permanent magnets. By implementing field weakening, the motor's speed can be extended beyond its rated speed range.During field weakening, the stator current is controlled in a way that intentionally weakens the magnetic field produced by the permanent magnets. This allows the motor to operate at higher speeds by reducing the magnetic flux linkage and adjusting the motor's torque-speed characteristics.The field weakening operation is typically achieved by controlling the d-axis current (also known as the magnetizing current) and q-axis current (also known as the torque-producing current) of the motor. By reducing the d-axis current and increasing the q-axis current, the balance between the magnetizing and torque-producing components of the current can be altered.
Field-Oriented Control (FOC), also known as Vector Control, is a control technique used in Permanent Magnet Synchronous Motors (PMSMs) to achieve precise control over motor speed and torque. FOC allows decoupled control of the motor's magnetizing flux and torque-producing current components, enabling efficient and accurate motor control.

##  Ambient
Ambient temperature as measured by a thermal sensor located closely to the stator.
The excitation magnetic field is provided by permanent magnet therefore the performance of PMSM is highly dependent on the permanent magnet (PM) temperature.
Temperature affects magnetism by either strengthening or weakening a magnet’s attractive force. A magnet subjected to heat experiences a reduction in its magnetic field as the particles within the magnet are moving at an increasingly faster and more sporadic rate. This jumbling confuses and misaligns the magnetic domains, causing the magnetism to decrease. Conversely, when the same magnet is exposed to low temperatures, its magnetic property is enhanced and the strength increases.
Since the magnetic property of permenant magnet is affected by the temperature, we measure the ambient temperature but we have temperature sensor near stator and in case of PMSM the permenant magnet is in the rotor there is some difference between the stator and rotor temperature.

## stator_yoke
Stator yoke temperature is measured with a thermal sensor.
Some effects of stator yoke surface temperature on PMSM :
Electrical Resistance: The stator yoke is typically made of a magnetic material with relatively high electrical conductivity. As the temperature of the stator yoke increases, its electrical resistance also tends to increase. This increased resistance can result in higher copper losses, reducing the motor's overall efficiency.
Core Losses: The stator yoke is a part of the motor's magnetic core, which can experience core losses due to hysteresis and eddy currents. Elevated temperatures can lead to increased core losses in the stator yoke, resulting in additional heat generation within the motor and reducing its efficiency.

stator_winding
Stator winding temperature measured with a thermal sensor.
Some effects of stator winding surface temperature on PMSM :
Electrical Resistance: The stator winding is made of conductive wire that carries the current. As the temperature of the stator winding increases, its electrical resistance also tends to increase. This increased resistance can result in higher copper losses, reduce the motor's overall efficiency, and lead to increased heat generation within the winding itself.

## Feature Selection
For Feature Engineering We Used Decision Tree to Find Important Features that hugely affect out Dependent Feature.

## Modeling & PreProcessing

We Used Both Linear and Non Linear Models and Variations of the same.
Main Models Used are :
SGD Regressor
Ordinary Least Square Model
Ridge Regressor
Random Forest Regressor
Catboost Regressor
Bayesian Ridge Regressor
KNN Regressor
Dense Model





