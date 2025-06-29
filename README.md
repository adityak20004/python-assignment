# python-assignment
Inputting Python
# 1. Revise sys.stdin Loop for Python 3
import sys

for line in sys.stdin:
    data = line.strip().split("\t")
    if len(data) == 6:
        date, time, store, item, cost, payment = data
        print("{0}\t{1}"). format(item, cost)

# 2. Add and Subtract Time with timedelta

from datetime import datetime, timedelta

now = datetime.now()

print("Current Time:", now)

# Add 1 day

print("Add 1 day:", now + timedelta(days=1))

# Subtract 60 seconds

print("Minus 60 seconds:", now - timedelta(seconds=60))

# Add 2 years 

print("Add 2 years:", now + timedelta(days= 2*365))

# Create a Timedelta Object for 100 Days, 10 Hours, and 13 Minutes

from datetime import timedelta

delta = timedelta(days=100, hours=10, minutes=13)

print("Timedelta:", delta)
print("Days:", delta.days)
print("Seconds:", delta.seconds)
print("Microseconds:", delta.microseconds)

# Function that Accepts Feet and Inches and Uses datetime

from datetime import datetime

def convert_to_inches(feet, inches):
    total_inches = feet * 12 +inches
    current_time = datetime.now()
    print(f"At time {current_time}, the total height is {total_inches} inches.")
    The output
    Current Time: 2025-06-29 21:52:58.780348
Add 1 day: 2025-06-30 21:52:58.780348
Minus 60 seconds: 2025-06-29 21:51:58.780348
Add 2 years: 2027-06-29 21:52:58.780348
Timedelta: 100 days, 10:13:00
Days: 100
Seconds: 36780
Microseconds: 0
At time 2025-06-29 21:52:58.780348, the total height is 68 inches.
At time 2025-06-29 21:52:58.780348, the total height is 72 inches.
At time 2025-06-29 21:52:58.780348, the total height is 59 inches
    return total_inches

# Example usage
convert_to_inches(5, 8)
convert_to_inches(6,0)
convert_to_inches(4,11)
