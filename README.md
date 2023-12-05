# tribonaci
def tribonacci(n):
    # Initialize the first three terms of the series
    sequence = [0, 1, 1]

    # If the number of terms required is less than or equal to 3
    if n <= 3:
        return sequence[:n]

    # Generate the Tribonacci sequence
    for i in range(3, n):
        next_term = sequence[i - 3] + sequence[i - 2] + sequence[i - 1]
        sequence.append(next_term)

    return sequence

# Input the number of terms for Tribonacci series
num_terms = int(input("Enter the number of terms for Tribonacci series: "))

# Generate and print the Tribonacci series
tribonacci_series = tribonacci(num_terms)
print(f"Tribonacci series up to {num_terms} terms: {tribonacci_series}")
