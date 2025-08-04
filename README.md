# 1.  Practice a simple python program
My first repository on GitHub
count = int(input())

# A simple Python program to read N numbers and search for a specific number X.

# Ask user for a positive integer N
N = int(input())

# Read N numbers one by one and store them in a list
numbers = []
for i in range(N):
    numbers.append(int(input()))

# Ask for the target number X
X = int(input())

# Check if X exists in the list and print its 1-based index or -1
if X in numbers:
    print(numbers.index(X) + 1)  # Convert to 1-based index
else:
    print(-1)
