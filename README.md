# 🌡️ Temperature Converter Program

# 📌 Task Description

This program converts temperatures between Celsius (°C), Fahrenheit (°F), and Kelvin (K).
It takes the temperature value and its unit as input, performs the conversion, and displays the output in the other two units.


---

# ✅ Features

✔ Converts from Celsius → Fahrenheit & Kelvin
✔ Converts from Fahrenheit → Celsius & Kelvin
✔ Converts from Kelvin → Celsius & Fahrenheit
✔ Simple and user-friendly command-line interface


---

# 🧮 Conversion Formulas Used

From → To	Formula

°C → °F	(°C × 9/5) + 32
°C → K	°C + 273.15
°F → °C	(°F − 32) × 5/9
°F → K	(°F − 32) × 5/9 + 273.15
K → °C	K − 273.15
K → °F	(K − 273.15) × 9/5 + 32



---

# 💻 Python Code

print("Temperature Converter Program")
temp = float(input("Enter the temperature value: "))
unit = input("Enter the unit (C/F/K): ").upper()

if unit == "C":
    f = (temp * 9/5) + 32
    k = temp + 273.15
    print(f"{temp}°C = {f}°F")
    print(f"{temp}°C = {k}K")

elif unit == "F":
    c = (temp - 32) * 5/9
    k = c + 273.15
    print(f"{temp}°F = {c}°C")
    print(f"{temp}°F = {k}K")

elif unit == "K":
    c = temp - 273.15
    f = (c * 9/5) + 32
    print(f"{temp}K = {c}°C")
    print(f"{temp}K = {f}°F")

else:
    print("Invalid unit! Please enter C, F, or K.")
