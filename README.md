# Solar-Wind-hybrid-system
# Solar-Wind Hybrid Energy System

print("==============================")
print("    SOLAR-WIND HYBRID SYSTEM")
print("==============================")

solar_power = float(input("Enter solar power generated (W): "))
wind_power = float(input("Enter wind power generated (W): "))
load_power = float(input("Enter load power required (W): "))

# Total renewable power
total_power = solar_power + wind_power

# Power balance
if total_power >= load_power:
    excess_power = total_power - load_power

    print("\n🟢 POWER AVAILABLE")
    print("Solar Power :", solar_power, "W")
    print("Wind Power  :", wind_power, "W")
    print("Total Power :", total_power, "W")
    print("Load Power  :", load_power, "W")
    print("Excess Power:", excess_power, "W")
    print("🔋 Excess energy can be stored in battery")

else:
    shortage = load_power - total_power

    print("\n🟡 POWER SHORTAGE")
    print("Solar Power :", solar_power, "W")
    print("Wind Power  :", wind_power, "W")
    print("Total Power :", total_power, "W")
    print("Load Power  :", load_power, "W")
    print("Power Shortage:", shortage, "W")
    print("🔋 Battery/Grid support required")

print("\nHybrid system monitoring completed.")
