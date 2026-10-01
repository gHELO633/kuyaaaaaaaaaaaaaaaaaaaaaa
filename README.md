Meal1 = ["mo1", "chickens meal", 120, 6]
Meal2 = ["mo2", "dessert meal ", 140, 10]
Meal3 = ["mo3", "pasta meal", 150, 8]

print("Display =Mo1 - chicken meal - 120 - Stock:", Meal1[3])
print("Display =Mo2 - chicken meal - 140 - Stock:", Meal2[3])
print("Display =Mo3 - chicken meal - 150 - Stock:", Meal3[3])

print("\nSimple order")
Your_choice = input("Your choice: ")
Quantity = int(input("Quantity: "))

if Your_choice == "mo1":
    if Quantity == 1:
        q = 1
    elif Quantity == 2:
        q = 2
    elif Quantity == 3:
        q = 3
    elif Quantity == 4:
        q = 4
    elif Quantity == 5:
        q = 5
    elif Quantity == 6:
        q = 6
    else:
        q = 0

    if q > 0:
        if q <= Meal1[3]:
            Total = Meal1[2] * q
            if Total >= 500:
                Discount = Total * 0.10
                Final_total = Total - Discount
            else:
                Discount = 0
                Final_total = Total
            Remaining_stock = Meal1[3] - q

            print("Your choice:", Meal1[1])
            print("Quantity:", q)
            print()
            print("Total:", Total)
            print("Discount:", f"{Discount:.2f}")
            print("Final total:", f"{Final_total:.2f}")
            print("Remaining stock:", Remaining_stock)
        else:
            print("Exceeds stock!")
    else:
        print("Invalid quantity!")

elif Your_choice == "mo2":
    if Quantity == 1:
        q = 1
    elif Quantity == 2:
        q = 2
    elif Quantity == 3:
        q = 3
    elif Quantity == 4:
        q = 4
    elif Quantity == 5:
        q = 5
    elif Quantity == 6:
        q = 6
    elif Quantity == 7:
        q = 7
    elif Quantity == 8:
        q = 8
    elif Quantity == 9:
        q = 9
    elif Quantity == 10:
        q = 10
    else:
        q = 0

    if q > 0:
        if q <= Meal2[3]:
            Total = Meal2[2] * q
            if Total >= 500:
                Discount = Total * 0.10
                Final_total = Total - Discount
            else:
                Discount = 0
                Final_total = Total
            Remaining_stock = Meal2[3] - q

            print("Your choice:", Meal2[1])
            print("Quantity:", q)
            print()
            print("Total:", Total)
            print("Discount:", f"{Discount:.2f}")
            print("Final total:", f"{Final_total:.2f}")
            print("Remaining stock:", Remaining_stock)
        else:
            print("Exceeds stock!")
    else:
        print("Invalid quantity!")

elif Your_choice == "mo3":
    if Quantity == 1:
        q = 1
    elif Quantity == 2:
        q = 2
    elif Quantity == 3:
        q = 3
    elif Quantity == 4:
        q = 4
    elif Quantity == 5:
        q = 5
    elif Quantity == 6:
        q = 6
    elif Quantity == 7:
        q = 7
    elif Quantity == 8:
        q = 8
    else:
        q = 0

    if q > 0:
        if q <= Meal3[3]:
            Total = Meal3[2] * q
            if Total >= 500:
                Discount = Total * 0.10
                Final_total = Total - Discount
            else:
                Discount = 0
                Final_total = Total
            Remaining_stock = Meal3[3] - q

            print("Your choice:", Meal3[1])
            print("Quantity:", q)
            print()
            print("Total:", Total)
            print("Discount:", f"{Discount:.2f}")
            print("Final total:", f"{Final_total:.2f}")
            print("Remaining stock:", Remaining_stock)
        else:
            print("Exceeds stock!")
    else:
        print("Invalid quantity!")

else:
    print("Wrong meal number/code!")
