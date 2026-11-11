# Temperature Monitor and Alarm Checker

## What it does
This program asks for 5 temperature readings from a machine and stores them in a list. It then prints the highest, lowest and average temperature, and warns you if any reading is above a safe limit. It repeats until you choose to quit.

## How to run it
Install Python 3, then run: python temperature_monitor.py

## Sample output
```
=== Temperature Monitor and Alarm Checker ===
Enter safe limit in °C (press Enter for 80.0): 40

Enter 5 temperature readings.
Reading 1 (°C): 22
Reading 2 (°C): 25
Reading 3 (°C): 28
Reading 4 (°C): 41
Reading 5 (°C): 45

----- RESULTS -----
Readings : [22.0, 25.0, 28.0, 41.0, 45.0]
Highest  : 45.0 °C
Lowest   : 22.0 °C
Average  : 32.2 °C
Limit    : 40.0 °C

Bar chart (each # = 2°C):
  1: ########### 22.0
  2: ############ 25.0
  3: ############## 28.0
  4: #################### 41.0  <-- OVER LIMIT
  5: ###################### 45.0  <-- OVER LIMIT

----- STATUS -----
WARNING: 2 reading(s) above the safe limit! Shut down or inspect the machine.
TREND ALERT: Temperature rose 3 times in a row. The machine may be overheating.

Check another machine? (y/n): n
Goodbye! Stay safe.
```

## My own twist
I added two features that were not in the brief:
1. **Text bar chart:** every reading is drawn as a row of `#` symbols (each one is 2°C), and readings over the limit are marked `<-- OVER LIMIT`, so you can see the pattern at a glance.
2. **Rising-trend alert:** if the temperature goes up 3 times in a row, the program warns that the machine may be overheating, even if the safe limit has not been reached yet.

I also let the user set their own safe limit (pressing Enter uses the default of 80°C) and added a "CAUTION" message when the highest reading is within 10% of the limit.

## What I learned
- User input can be wrong, so I check it with `try/except` before using it, instead of letting the program crash.
- Breaking a program into small functions makes it easier to read, test and fix.

## Author
Your name, ND1 Mechatronics Engineering Engineering, YabaTech.
# Divine-temperature-monitor_alarm-checker-
