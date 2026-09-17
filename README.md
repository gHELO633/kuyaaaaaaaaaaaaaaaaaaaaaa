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

# Transportation Selection
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

trans_price = price

# Baggage Information using ONLY IF/ELIF/ELSE (Up to 50 Travelers)
print("\n--- Baggage Information ---")
print("Standard Limit: 15kg per traveler")
print("Excess Fee: ₱100 per kg over limit")

total_baggage_fee = 0.0

# Traveler 1 to 50 sequentially checked using IF statements
if travelers >= 1:
    w = float(input("Enter baggage weight for Traveler 1 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 2:
    w = float(input("Enter baggage weight for Traveler 2 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 3:
    w = float(input("Enter baggage weight for Traveler 3 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 4:
    w = float(input("Enter baggage weight for Traveler 4 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 5:
    w = float(input("Enter baggage weight for Traveler 5 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 6:
    w = float(input("Enter baggage weight for Traveler 6 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 7:
    w = float(input("Enter baggage weight for Traveler 7 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 8:
    w = float(input("Enter baggage weight for Traveler 8 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 9:
    w = float(input("Enter baggage weight for Traveler 9 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 10:
    w = float(input("Enter baggage weight for Traveler 10 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 11:
    w = float(input("Enter baggage weight for Traveler 11 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 12:
    w = float(input("Enter baggage weight for Traveler 12 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 13:
    w = float(input("Enter baggage weight for Traveler 13 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 14:
    w = float(input("Enter baggage weight for Traveler 14 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 15:
    w = float(input("Enter baggage weight for Traveler 15 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 16:
    w = float(input("Enter baggage weight for Traveler 16 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 17:
    w = float(input("Enter baggage weight for Traveler 17 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 18:
    w = float(input("Enter baggage weight for Traveler 18 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 19:
    w = float(input("Enter baggage weight for Traveler 19 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 20:
    w = float(input("Enter baggage weight for Traveler 20 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 21:
    w = float(input("Enter baggage weight for Traveler 21 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 22:
    w = float(input("Enter baggage weight for Traveler 22 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 23:
    w = float(input("Enter baggage weight for Traveler 23 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 24:
    w = float(input("Enter baggage weight for Traveler 24 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 25:
    w = float(input("Enter baggage weight for Traveler 25 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 26:
    w = float(input("Enter baggage weight for Traveler 26 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 27:
    w = float(input("Enter baggage weight for Traveler 27 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 28:
    w = float(input("Enter baggage weight for Traveler 28 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 29:
    w = float(input("Enter baggage weight for Traveler 29 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 30:
    w = float(input("Enter baggage weight for Traveler 30 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 31:
    w = float(input("Enter baggage weight for Traveler 31 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 32:
    w = float(input("Enter baggage weight for Traveler 32 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 33:
    w = float(input("Enter baggage weight for Traveler 33 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 34:
    w = float(input("Enter baggage weight for Traveler 34 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 35:
    w = float(input("Enter baggage weight for Traveler 35 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 36:
    w = float(input("Enter baggage weight for Traveler 36 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 37:
    w = float(input("Enter baggage weight for Traveler 37 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 38:
    w = float(input("Enter baggage weight for Traveler 38 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 39:
    w = float(input("Enter baggage weight for Traveler 39 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 40:
    w = float(input("Enter baggage weight for Traveler 40 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 41:
    w = float(input("Enter baggage weight for Traveler 41 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 42:
    w = float(input("Enter baggage weight for Traveler 42 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 43:
    w = float(input("Enter baggage weight for Traveler 43 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 44:
    w = float(input("Enter baggage weight for Traveler 44 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 45:
    w = float(input("Enter baggage weight for Traveler 45 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 46:
    w = float(input("Enter baggage weight for Traveler 46 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 47:
    w = float(input("Enter baggage weight for Traveler 47 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 48:
    w = float(input("Enter baggage weight for Traveler 48 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 49:
    w = float(input("Enter baggage weight for Traveler 49 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

if travelers >= 50:
    w = float(input("Enter baggage weight for Traveler 50 (kg): "))
    if w > 15: total_baggage_fee += (w - 15) * 100

# Base Calculations
tour_subtotal = price * travelers
trans_subtotal = trans_price * travelers
base_total = tour_subtotal + trans_subtotal

# Group Discount
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
