account_1 = ["1001", "juan", 1111, 5000]
account_2 = ["1002", "maria", 2222, 10000]

print("======= SIMPLE ATM ============")
account_number = input("enter account number: ")
pin = int(input("enter pin: "))

if account_number == account_1[0] and pin == account_1[2]:
    print(f"welcome {account_1[1]}")
    print(f"balance: {account_1[3]}")

    print("1. deposit")
    print("2. withdraw")

    choice = input("enter choice: ")
    if choice == "1":
        amount = float(input("enter deposit amount: "))

        if amount > 0:
            account_1[3] = account_1[3] + amount
            print("deposit successful")
            print(f"new balance: {account_1[3]}")

        else:
            print("invalid amount")

    elif choice == "2":
        amount = float(input("enter withdrawal amount: "))

        if amount > 0 and amount <= account_1[3]:
            account_1[3] = account_1[3] - amount
            print("withdrawal successful")
            print(f"new balance: {account_1[3]}")

        elif amount <= 0 or amount > account_1[3]:
            print("invalid amount or insufficient balance")

        else:
            print("invalid amount")

    else:
        print("invalid choice")

elif account_number == account_2[0] and pin == account_2[2]:
    print(f"welcome {account_2[1]}")
    print(f"balance: {account_2[3]}")

    print("1. deposit")
    print("2. withdraw")

    choice = input("enter choice: ")
    if choice == "1":
        amount = float(input("enter deposit amount: "))

        if amount > 0:
            account_2[3] = account_2[3] + amount
            print("deposit successful")
            print(f"new balance: {account_2[3]}")

        else:
            print("invalid amount")

    elif choice == "2":
        amount = float(input("enter withdrawal amount: "))

        if amount > 0 and amount <= account_2[3]:
            account_2[3] = account_2[3] - amount
            print("withdrawal successful")
            print(f"new balance: {account_2[3]}")

        elif amount <= 0 or amount > account_2[3]:
            print("invalid amount or insufficient balance")

        else:
            print("invalid amount")

    else:
        print("invalid choice")

else:
    print("invalid account number or pin")
