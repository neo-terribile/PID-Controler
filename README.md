# PID-Controler

Aufgeteilt in 3 Dateien. Der Header beinhaltet die Datentypen der Variablen.\
PID enthält die Funktionen PIDControllerInit zum zurücksetzen der Variablen am beginn der Regelung,\
sowie PIDControllUpdate für die laufende Regelung.\
In main werden die Anfangsparameter definiert und die Regelung für die dauer der vorgegebene Zeit gestartet.

Note on 'derivative-on-measurement': Since the 'error signal' effectively going into the differentiator does not depend on the setpoint: e[n] = 0 - measurement, and therefore (e[n] - e[n - 1]) = (0 - measurement) - (0 - prevMeasurement) = -Kd * (measurement - prevMeasurement). (Note the minus sign compared to derivative-on-error!) I've included the minus sign in the code, so gains will have the effect as normal.
