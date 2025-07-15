# Создайте функцию, которая принимает в качестве параметра - натуральное целое число.     Данная функция находит факториал полученного числа  Например, факториал числа 3 это число 6.      Теперь создайте список факториалов чисел от получившегося ранее факториала 6, до 1.  
# Решение:
def factorial(n):
    if n < 0:
        return None
    elif n == 0 or n == 1:
        return 1
    else:
        result = 1
        for i in range(2, n + 1):
            result *= i
        return result

def list_of_factorials(start):
    factorials = []
    for i in range(start, 0, -1):
        factorials.append(factorial(i))
    return factorials
number = int(input("Введите натуральное целое число: "))
factorial_of_number = factorial(number)

print(f"Факториал числа {number} = {factorial_of_number}")
result_list = list_of_factorials(factorial_of_number)
print("Список факториалов в убывающем порядке:", result_list)
