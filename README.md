expenses = []

while True:
    print("\n----- EXPENSE TRACKER -----")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Show Total")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        amount = float(input("Enter expense amount: "))
        expenses.append(amount)
        print("Expense added successfully!")

    elif choice == "2":
        print("\nYour Expenses:")

        if len(expenses) == 0:
            print("No expenses found.")
        else:
            for expense in expenses:
                print(expense)

    elif choice == "3":
        total = sum(expenses)
        print("Total Expenses:", total)

    elif choice == "4":
        print("Exiting....")
        break

    else:
        print("Invalid choice!")
