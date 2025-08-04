# 1.  Practice a simple python program
My first repository on GitHub
count = int(input())

# A simple Python program to read N numbers and search for a specific number X.

def run_program():
    """
    Main function to run the number-input and search process.
    """
    # 1. Get a positive integer N from the user.
    #    This loop ensures a valid positive integer is entered.
    while True:
        try:
            n_input = input("Please enter a positive integer N: ")
            n = int(n_input)
            if n > 0:
                break
            else:
                print("N must be a positive integer. Please try again.")
        except ValueError:
            print("Invalid input. Please enter a valid integer.")

    # 2. Read N numbers from the user, one by one.
    numbers = []
    print(f"\nPlease enter {n} numbers, one by one:")
    for i in range(n):
        while True:
            try:
                num_input = input(f"Enter number {i + 1}: ")
                num = int(num_input)
                numbers.append(num)
                break
            except ValueError:
                print("Invalid input. Please enter a valid integer.")

    # 3. Get the integer X to search for.
    #    This loop ensures a valid integer is entered.
    while True:
        try:
            x_input = input("\nPlease enter the integer X to search for: ")
            x = int(x_input)
            break
        except ValueError:
            print("Invalid input. Please enter a valid integer.")

    # 4. Search for X in the list of numbers.
    index_found = -1
    # Iterate through the list to find the first occurrence of X.
    for i in range(len(numbers)):
        if numbers[i] == x:
            # If X is found, store its 1-based index and exit the loop.
            index_found = i + 1
            break
    
    # 5. Print the result.
    print(index_found)

# Run the program
if __name__ == "__main__":
    run_program()
