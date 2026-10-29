# annabellao854.github.io
https://www.w3schools.com/html/default.asp

# Annabella Orozco
# basic calculator app

print("Hello", end='! ')
print("Welcome to a Python Calculator.")
print("You'll be able to do simple calculations such as",end= ": ")
print("addition", "subtraction","and more.", sep=", ")
print("Ready to get started?")
print("Follow the instructions below.")

def add(a, b):
    return a + b
    # the "+" signs will add the numbers

def subtract(a, b):
    return a - b
    # the "-" sign will subtract the two numbers

def multiply(a, b):
    return a * b
    # the "*" sign will multiply the numbers

def exponent(a, b):
    return a ** b
    # the "**" raises the number to the exponent

def divide(a, b):
    if b == 0:
        return "Error: Division by zero. Please try again."
    return a / b
    # the "/" will divide the numbers

def floor_division(a, b):
    if b == 0:
        return "Error: Division by zero. Please try again."
    return a // b
    # the "//" divides two numbers and rounds the result down to the
    # nearest whole number

def modulus(a, b):
    if b == 0:
        return "Error: Modulus by zero. Please try again."
    return a % b
    # the "%"  calculates the remainder of a division operation, telling you
    # what is left over

def run_calculator():
    doAgain = "y"
    while doAgain == "y":

        print("\n""Select operation")
        print("1. Addition")
        print("2. Subtraction")
        print("3. Multiplication")
        print("4. Exponent")
        print("5. Divide")
        print("6. Floor Division")
        print("7. Modulus")
        print("8. End Program")

        choice = input("Enter your choice 1-8: ")
        if choice and int(choice) in range (1,8):
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
            if choice == "1":
                res = add(num1, num2)

            elif choice == "2":
                res = subtract(num1, num2)

            elif choice == "3":
                res = multiply(num1, num2)

            elif choice == "4":
                res = exponent(num1, num2)

            elif choice == "5":
                res = divide(num1, num2)

            elif choice == "6":
                res = floor_division(num1, num2)

            elif choice == "7":
                res = modulus(num1, num2)

            print("Result:", res, "\n")
            choice_doAgain = input("Type 'y' to run the program again or "
                                    "anything "
                               "else "
                           "to quit.")

        if choice == "8" or choice_doAgain <= "x" or choice_doAgain == "z":
            doAgain = not True
            print("\n""Thank you for using this calculator. " +
                              "Hope you "
                                                                   "enjoyed it!")

        ValueError
        if choice <= "0" or choice > "8" or choice == "":
            print("\n""Out of range. Please try again.""\n")

if __name__ == "__main__":
    run_calculator()
