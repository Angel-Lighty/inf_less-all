# Вопросы
1. 
Статистика изучает методы сбора, анализа, интерпретации и представления количественных данных. Основная задача статистики — извлечение информации из данных для принятия обоснованных решений, выявление закономерностей и трендов, а также оценка вероятностей различных событий.

2. 
- Функция COUNT игнорирует пустые ячейки и считает только ячейки с числовыми значениями.
- Функция AVERAGE также игнорирует пустые ячейки, однако, если все ячейки в выбранном диапазоне пустые, функция вернёт ошибку (#DIV/0!), так как деление на ноль невозможно.

3.
- COUNT считает общее количество ячеек с числовыми значениями в заданном диапазоне.
- COUNTIF считает количество ячеек, которые соответствуют заданному условию (например, ячейки, содержащие определённое значение).

4.
Среднеквадратическое отклонение — это мера разброса значений в наборе данных относительно их среднего значения. Чем меньше значение квадратного отклонения, тем больше данные сконцентрированы вокруг среднего, и наоборот.

5. 
Коэффициент корреляции показывает степень взаимосвязи между двумя переменными. Значение может варьироваться от -1 до 1. Значение 1 указывает на сильную прямую зависимость, -1 — на сильную обратную зависимость, а 0 — на отсутствие зависимости.

6. 
Коэффициент -0.5 указывает на умеренную обратную связь между двумя рядами данных. Это означает, что, как правило, с увеличением значений одного ряда, значения другого ряда будут снижаться, но эта зависимость не является очень сильной.

7.
Коэффициент 0.1 указывает на очень слабую положительную корреляцию. Это означает, что существует незначительная тенденция к увеличению значений одного ряда при увеличении значений другого, но эта связь практически незначима.

 Задачи

1.
- Из формулы SUM(B1:B2) = 5, имеем \( B1 + B2 = 5 \).
- Из формулы AVERAGE(B1:B3) = 3, имеем \( (B1 + B2 + B3) / 3 = 3 \) или \( B1 + B2 + B3 = 9 \).
- Подставляя первое уравнение во второе: \( 5 + B3 = 9 \) → \( B3 = 4 \).

2. 
- Из SUM(C3:E3) = 12 знаем, что сумма ячеек C3, D3 и E3 равна 12.
- Значение AVERAGE(C3:F3) = (SUM(C3:E3) + F3) / 4 = (12 + 4) / 4 = 16 / 4 = 4.

3. 
- Из SUM(A2:D2) = 12 знаем, что сумма ячеек A2, B2, C2 и D2 равна 12.
- Значение AVERAGE(A2:E2) = (SUM(A2:D2) + E2) / 5 = (12 + 13) / 5 = 25 / 5 = 5.

4. 
- Значение SUM(A6:D6) = A6 + B6 + C6 + D6 = -6 + 6 = 0.

5. 
- Из AVERAGE(B5:E5) = 10 имеем \( (B5 + C5 + D5 + E5) / 4 = 10 \) или \( B5 + C5 + D5 + E5 = 40 \).
- Таким образом, SUM(B5:F5) = B5 + C5 + D5 + E5 + F5 = 40 + 1 = 41.

6. 
- Из \( (A1 + B1 + C1) / 3 = 6 \) имеем \( A1 + B1 + C1 = 18 \).
- Значение SUM(A1:D1) = A1 + B1 + C1 + D1 = 7, следовательно \( 18 + D1 = 7\), откуда \( D1 = 7 - 18 = -11 \).

7.
- Если =AVERAGE(A3:D4) = 6, значит сумма всех 8 ячеек в области = \( 8 \times 6 = 48 \).
- Мы знаем, что SUM(D3:D4) = 6, значит \( \text{SUM(A3:C4)} = 48 - 6 = 42 \).
- Поскольку размер области \( A3:C4 \) равен 6 ячейкам \( (2 \times 3) \), то =AVERAGE(A3:C4) = 42 / 6 = 7.

8. 
- Сумма между C2:D4 это \( 3 \times 6 = 18\), значит \( \text{SUM(C5:D5)} = 16 - 18 = -2 \).

9. 
Если формулы в C3 зависели от значений в B2 или B3, то значение C3 изменится в зависимости от того, как пересчитаются использованные ячейки в связанных формулах. Если C3 использует значение из B2, тогда оно изменится; если нет, то останется прежним.

10. 
``excel
=IF(C2="да", 200, B2200 + (A2-1)200)
`
Эта формула устанавливает, что если лифт есть (значение "да"), стоимость доставки фиксирована, иначе считается по этажам.

11. 
=IF(AND(B2>=80, C2>=80), "да", "нет")
`
Эту формулу использовать для проверки, получено ли не менее 80 баллов в каждом из туров собеседования.

12.
`excel
=IF(OR(B2>=90, C2>=90), "да", "нет")
`
Формула проверяет, хотя бы в одном туре количество баллов равняется или превышает 90.

13. 
`excel
=IF(B2 > TIME(20, 0, 0), IF(A2=1, 2, 5), 5)
`
Эта формула учитывает условия применения сниженного тарифа.

14. 
`excel
=IF(B2 > 1000, B2*0.95, B2)
`
Эта формула применяет скидку 5%, если цена превышает 1000 рублей.

15. 
`excel
=IF(C2 > 6, IF(B2 > 1000, B20.8, B20.9), B2)
``