# Prime-just-less-than-number
You're given a number n. Find the largest prime number less than or equal to n. Input You are given an integer n ( 7 &lt;= n &lt;= 105). Output Print an integer, representing the largest prime number less than or equal to n.

def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

def largest_prime_less_than_or_equal_to_n(n):
    for i in range(n, 1, -1):
        if is_prime(i):
            return i

n = int(input())

result = largest_prime_less_than_or_equal_to_n(n)
print(result)
