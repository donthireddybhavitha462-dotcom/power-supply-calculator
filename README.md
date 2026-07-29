# ==========================================
#        POWER SUPPLY MANAGEMENT SYSTEM
# ==========================================

print("=" * 50)
print("        POWER SUPPLY MANAGEMENT SYSTEM")
print("=" * 50)

device_name = input("Enter Device Name: ")

voltage = float(input("Enter Supply Voltage (Volts): "))
current = float(input("Enter Current (Amps): "))
hours = float(input("Enter Usage Time (Hours): "))

# Power Calculation
power = voltage * current

# Energy Calculation
energy = power * hours

# Monthly Energy
monthly_energy = energy * 30

# Electricity Cost
rate = float(input("Enter Electricity Cost per kWh: "))

energy_kwh = monthly_energy / 1000
bill = energy_kwh * rate

print("\n" + "=" * 50)
print("             POWER REPORT")
print("=" * 50)

print(f"Device Name          : {device_name}")
print(f"Voltage              : {voltage} V")
print(f"Current              : {current} A")
print(f"Power                : {power:.2f} W")
print(f"Daily Usage          : {hours} Hours")
print(f"Daily Energy         : {energy:.2f} Wh")
print(f"Monthly Energy       : {monthly_energy:.2f} Wh")
print(f"Monthly Energy(kWh)  : {energy_kwh:.2f} kWh")
print(f"Estimated Bill       : {bill:.2f}")

print("\nPower Status")
if power < 50:
    print("Low Power Device")
elif power < 500:
    print("Medium Power Device")
else:
    print("High Power Device")

print("\nEfficiency Check")
if hours <= 4:
    print("Excellent usage. Power consumption is low.")
elif hours <= 8:
    print("Average usage. Try reducing operating hours.")
else:
    print("High usage detected. Consider saving electricity.")

print("\nSafety Suggestions")
print("- Use a quality power supply.")
print("- Avoid overloading sockets.")
print("- Check wiring regularly.")
print("- Turn OFF devices when not in use.")
print("- Use surge protectors for sensitive equipment.")

print("\nVoltage Condition")
if voltage < 200:
    print("Warning: Low Voltage")
elif voltage > 250:
    print("Warning: High Voltage")
else:
    print("Voltage is Normal")

print("\nCurrent Condition")
if current > 10:
    print("High Current Detected")
else:
    print("Current is within Safe Limit")

print("\nThank you for using the Power Supply Management System!")
