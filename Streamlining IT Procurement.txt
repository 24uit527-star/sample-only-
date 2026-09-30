# Streamlining IT Procurement
# Automating Standard Laptop Orders

print("==============================================")
print("       IT PROCUREMENT AUTOMATION SYSTEM")
print("==============================================")

# Employee details
employee_name = input("Enter Employee Name: ")
employee_id = input("Enter Employee ID: ")
department = input("Enter Department: ")

print("\nLaptop Types:")
print("1. Standard Laptop")
print("2. High Performance Laptop")
print("3. Developer Laptop")

laptop_choice = int(input("Select Laptop Type (1-3): "))
quantity = int(input("Enter Laptop Quantity: "))

print("\n----------------------------------------------")
print("             ORDER DETAILS")
print("----------------------------------------------")

print("Employee Name :", employee_name)
print("Employee ID   :", employee_id)
print("Department    :", department)
print("Quantity      :", quantity)

# Laptop selection
if laptop_choice == 1:
    laptop_type = "Standard Laptop"
    price = 50000

elif laptop_choice == 2:
    laptop_type = "High Performance Laptop"
    price = 75000

elif laptop_choice == 3:
    laptop_type = "Developer Laptop"
    price = 85000

else:
    print("Invalid laptop type selected.")
    exit()

print("Laptop Type   :", laptop_type)
print("Price/Laptop  : Rs.", price)

# Calculate total amount
total_amount = price * quantity

print("Total Amount  : Rs.", total_amount)

print("\n----------------------------------------------")
print("          PROCUREMENT PROCESS")
print("----------------------------------------------")

# Automation for standard laptop
if laptop_choice == 1:

    print("Standard laptop order detected.")
    print("Checking stock availability...")

    stock = 10

    if quantity <= stock:

        print("Stock Status  : Available")
        print("Creating procurement request...")

        # Approval process
        print("Sending request for approval...")

        approval = input("Enter approval status (Approved/Rejected): ")

        if approval.lower() == "approved":

            print("\nApproval Status : Approved")
            print("Creating procurement task...")

            task_id = "PROC-" + employee_id

            print("Procurement Task ID :", task_id)
            print("Assigned To         : IT Procurement Team")
            print("Order Status        : Processing")

            print("\n----------------------------------------------")
            print("        LAPTOP ORDER SUCCESSFUL")
            print("----------------------------------------------")

            print("Employee       :", employee_name)
            print("Department     :", department)
            print("Laptop         :", laptop_type)
            print("Quantity       :", quantity)
            print("Total Amount   : Rs.", total_amount)
            print("Task ID        :", task_id)
            print("Status         : Processing")

        else:

            print("\nApproval Status : Rejected")
            print("Laptop order has been rejected.")
            print("No procurement task was created.")

    else:

        print("Stock Status : Not Available")
        print("Requested quantity is greater than available stock.")
        print("Order cannot be processed.")

# Non-standard laptop
else:

    print("Non-standard laptop order detected.")
    print("Additional approval is required.")

    approval = input("Enter manager approval (Approved/Rejected): ")

    if approval.lower() == "approved":

        print("Manager Approval : Approved")
        print("Creating manual procurement request...")
        print("Assigned To : IT Procurement Team")
        print("Order Status : Manual Processing")

    else:

        print("Manager Approval : Rejected")
        print("Order has been rejected.")

print("\n==============================================")
print("       IT PROCUREMENT PROCESS COMPLETED")
print("==============================================")