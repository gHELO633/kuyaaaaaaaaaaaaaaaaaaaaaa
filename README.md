import sys

print("")
print(" WELCOME TO TRAVEL & TOUR SYSTEM")
print("")

print("\nAvailable Tour Packages:")
print("1. Boracay Island - ₱3,500 per person")
print("2. Baguio City - ₱2,500 per person")
print("3. Palawan Adventure - ₱5,000 per person")
print("4. Cebu Getaway - ₱4,000 per person")

name = input("\nEnter your name: ")

# Package Selection
choice = input("Enter package number (1-4): ")

if choice == "1":
    destination = "Boracay Island"
    price = 3500
elif choice == "2":
    destination = "Baguio City"
    price = 2500
elif choice == "3":
    destination = "Palawan Adventure"
    price = 5000
elif choice == "4":
    destination = "Cebu Getaway"
    price = 4000
else:
    print("\nInvalid package choice. Please restart.")
    sys.exit()

# Travelers Input with Validation (Max 50)
travelers = int(input("Enter number of travelers (Max 50): "))
if travelers < 1 or travelers > 50:
    print("\nInvalid number of travelers. Allowed range is 1 to 50.")
    sys.exit()

# Transportation Selection (Uses the package fee as the per-person transport cost)
print(f"\nTransportation Options (Fee matches package price: ₱{price:,.2f} per person):")
print("1. Bus")
print("2. Airplane")
print("3. Ship")

trans_choice = input("Choose transportation mode (1-3): ")

if trans_choice == "1":
    transport = "Bus"
elif trans_choice == "2":
    transport = "Airplane"
elif trans_choice == "3":
    transport = "Ship"
else:
    print("\nInvalid transportation choice. Please restart.")
    sys.exit()

# Set transport rate equal to package price
trans_price = price

# Baggage Weight Input & Excess Fee Calculation using an Iterative Loop
print("\n--- Baggage Information ---")
print("Standard Limit: 15kg per traveler")
print("Excess Fee: ₱100 per kg over limit")

total_baggage_fee = 0.0
current_traveler = 1

while True:
    if current_traveler > travelers:
        break
    else:
        weight = float(input(f"Enter baggage weight for Traveler {current_traveler} (kg): "))
        if weight > 15:
            excess = weight - 15
            total_baggage_fee += excess * 100
        elif weight <= 15:
            pass
        else:
            pass
        current_traveler += 1

# Base Calculations
tour_subtotal = price * travelers
trans_subtotal = trans_price * travelers
base_total = tour_subtotal + trans_subtotal

# Group Discount (Applied to combined base cost)
if travelers >= 5:
    discount = base_total * 0.10
    discount_name = "10% Group Discount"
elif travelers >= 3:
    discount = base_total * 0.05
    discount_name = "5% Group Discount"
else:
    discount = 0
    discount_name = "No Group Discount"

final_total = (base_total - discount) + total_baggage_fee

# Booking Summary
print("\n==========================================")
print(" BOOKING SUMMARY")
print("")
print(f"Customer Name    : {name}")
print(f"Destination      : {destination}")
print(f"Transportation   : {transport}")
print(f"Travelers        : {travelers}")
print(f"Package Subtotal : ₱{tour_subtotal:,.2f}")
print(f"Transport Subtotal: ₱{trans_subtotal:,.2f}")
print(f"Discount         : {discount_name} (-₱{discount:,.2f})")
print(f"Baggage Fees     : ₱{total_baggage_fee:,.2f}")
print("------------------------------------------")
print(f"TOTAL AMOUNT     : ₱{final_total:,.2f}")
print("")

# Payment Processing
cash = float(input("\nEnter cash amount : ₱"))

if cash < final_total:
    print(f"Insufficient cash! You still owe ₱{final_total - cash:,.2f}.")
else:
    change = cash - final_total
    print(f"Payment Received : ₱{cash:,.2f}")
    print(f"Change           : ₱{change:,.2f}")
    print("\nThank you for booking with us! Have a safe trip.")
