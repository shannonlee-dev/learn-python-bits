import sys

def generate_binary_numbers(n):
    """Generates and prints n-bit binary numbers."""
    for i in range(2**n):
        print(bin(i)[2:].zfill(n))

if __name__ == "__main__":
    # Check if an argument is provided
    if len(sys.argv) != 2:
        print("Usage: python main.py <number_of_bits>")
        print("Example: python main.py 5")
        sys.exit(1)

    try:
        # Try to convert the argument to an integer
        num_bits = int(sys.argv[1])
        
        # Check if the number is a non-negative integer
        if num_bits < 0:
            raise ValueError("Number of bits cannot be negative.")
            
        generate_binary_numbers(num_bits)

    except ValueError as e:
        # Handle cases where the input is not a valid integer or is negative
        print(f"Error: Invalid input. Please provide a non-negative integer.")
        print(f"Details: {e}")
        sys.exit(1)
