#1. Напишите программу, которая принимает на вход цифру, обозначающую день недели, и проверяет, является ли этот день выходным.
#Пример:
#- 6 -> да
#- 7 -> да
#- 1 -> нет

day_of_week = int(input('Введите день недели: '))
if day_of_week <= 5 and day_of_week >= 1:
    print('Weekdays')
elif day_of_week == 6 or day_of_week == 7:
    print('Day off')
else:
    print('Error')
    
#2 .Напишите программу для. проверки истинности утверждения ¬(X ⋁ Y ⋁ Z) = ¬X ⋀ ¬Y ⋀ ¬Z 
# расшифровка этого выражения not (x[0] or x[1] or x[2] = not x[0] and not x[1] and not x[2]) для всех значений предикат.

x1 = int(input('Введите х: '))
x2 = int(input('Введите y: '))
x3 = int(input('Введите z: '))

n1 = not (x1 or x2 or x3) 
n2 = not x1 and not x2 and not x3

if n1 == n2:
    print('True')
else:
    print('False')
    
#3 .Напишите программу, которая принимает на вход координаты точки (X и Y), причём X ≠ 0 и Y ≠ 0 и выдаёт номер четверти плоскости, в которой находится эта точка .
#Пример:
#- x=34; y=-30 -> 4
#- x=2; y=4-> 1
#- x=-34; y=-30 -> 3

x = int(input('Введите х: '))
y = int(input('Введите y: '))


if x > 0 and y > 0:
    print('1 quarter')
elif x > 0 and y < 0:
    print('4 quarter')
elif x < 0 and y < 0:
    print('3 quarter')
elif x < 0 and y > 0:
    print('2 quarter')   
elif x == 0 and y == 0:
    print('error') 


# Второй вариант, оптимизированнее

'''
if x > 0:
    if y > 0:
        print('1 quarter')
    else:
        print('4 quarter')
elif x < 0:
    if y > 0:
        print('2 quarter')
    else:
        print('3 quarter')
else:
    print('Error')
'''

#4. Напишите программу, которая по заданному номеру четверти, показывает диапазон возможных координат точек в этой четверти (x и y).

number_quarter = int(input('Введите номер четверти: '))
x = range(1,10)
y = range(-10,-1)
if number_quarter == 1:
    print(f'x = {x}')
    print(f'y = {x}')
elif number_quarter == 2:
    print(f'x = {y}')
    print(f'y = {x}')
elif number_quarter == 3:
    print(f'x = {y}')
    print(f'y = {y}')
elif number_quarter == 4:
    print(f'x = {x}')
    print(f'y = {y}')
    
#5 .Напишите программу, которая принимает на вход координаты двух точек и находит расстояние между ними в 2D пространстве.
#Пример:
#- A (3,6); B (2,1) -> 5,09
#- A (7,-5); B (1,-1) -> 7,21
import math
list = []
for i in range(4):
    list.append(int(input('Введите элементы: ')))

# x1*x2+y1*y2

distans = math.sqrt(float(list[0] - list[2])** 2 + (list[1] - list[3]) ** 2)
print (round(distans, 2))
