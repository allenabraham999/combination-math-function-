# combination-math-function-
a simple program to find the combination of two nos(ncr)
import math


def get_factorial(m):
    if m < 0:
        print("sorry! you have entered an invalid choice")
    elif m == 0:
        return 1
    elif m > 0:
        y = 1
        for i in range(1, m + 1):
            y *= i
        return y


def combination(n, r):
    if float(n).is_integer() and float(r).is_integer():
        if n < r:
            print("soory! n value has to be higher than the r value")
        else:
            total = get_factorial(n) // (get_factorial(n - r) * get_factorial(r))
            return total
    else:
        print("you have entered wrong values")


print(combination(6, 4))
