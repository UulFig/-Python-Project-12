# -Python-Project-12
#12 Does a number is Odd or Even ? 2.0

print("Hello! Let\'s check if a number is odd or even!\n")

def main():
    def inputnumber():
        while True:
            inputnumber = input("Please, put a number: ")
            if not inputnumber.isdigit():
                print("Please, use a valid number!\n")
            else:
                return inputnumber

    def yes_no(message):
        while True:
            userinput = input(message).lower()
            if userinput == "yes":
                return True
            elif userinput == "no":
                return False
            else:
                return yes_no("Please, use 'yes' or 'no'.\n")

    number = inputnumber()
    if int(number) % 2 == 1:
        print(f"{number} is odd.\n")
    else:
        print(f"{number} is even.\n")

    while True:
        if yes_no("Do you want to try again?\n"):
            return main()
        else:
            print("Good bye!")
            return


main()
