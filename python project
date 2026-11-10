
# Resistor Combination Calculator
# CTE213 Python Mini Project
# Author: Ashibogwu Oscar

# Function to calculate total resistance in series
def calculate_series(resistors):
    total = sum(resistors)
    return total


# Function to calculate total resistance in parallel
def calculate_parallel(resistors):
    reciprocal_sum = 0

    for resistance in resistors:
        reciprocal_sum += 1 / resistance

    total = 1 / reciprocal_sum
    return total


# Function to display the results
def display_results(series, parallel):

    print("\n===== CALCULATION RESULTS =====")

    print(f"Total resistance in series: {series:.2f} ohms")
    print(f"Total resistance in parallel: {parallel:.2f} ohms")

    # Our own twist: Compare both results
    print("\n===== RESISTANCE COMPARISON =====")

    if series > parallel:
        print("Series connection has higher resistance.")
    elif parallel > series:
        print("Parallel connection has higher resistance.")
    else:
        print("Both connections have equal resistance.")


# Main program
def main():

    resistors = []

    print("================================")
    print("   RESISTOR COMBINATION CALCULATOR")
    print("================================")

    # Get the number of resistors
    while True:
        try:
            number = int(input("\nEnter number of resistors: "))

            if number > 0:
                break
            else:
                print("Please enter a number greater than zero.")

        except ValueError:
            print("Invalid input. Enter a whole number.")

    # Collect resistor values
    for i in range(number):

        while True:
            try:
                value = float(input(
                    f"Enter resistance of resistor {i + 1} (ohms): "
                ))

                if value > 0:
                    resistors.append(value)
                    break
                else:
                    print("Resistance must be greater than zero.")

            except ValueError:
                print("Invalid input. Enter a numerical value.")

    # Perform calculations
    series_result = calculate_series(resistors)
    parallel_result = calculate_parallel(resistors)

    # Display final results
    display_results(series_result, parallel_result)


# Run the program
if __name__ == "__main__":
    main()
