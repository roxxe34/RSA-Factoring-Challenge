#!/usr/bin/python3
import sys

def factorize(n):
    for i in range(2, n):
        if n % i == 0:
            return i, n // i
    return None, None

def main(filename):
    try:
        with open(filename, 'r') as file:
            for line in file:
                number = int(line.strip())
                p, q = factorize(number)
                if p is not None and q is not None:
                    print(f"{number}={p}*{q}")
                else:
                    print(f"Unable to factorize {number}")
    except FileNotFoundError:
        print("File not found.")

if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
    else:
        filename = sys.argv[1]
        main(filename)

