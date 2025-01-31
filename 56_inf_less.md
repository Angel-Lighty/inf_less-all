# Вопросы
1. Существует несколько типов данных: целые числа, вещественные числа, символы, строки, логические значения и перечисления.

2. В разных языках программирования несколько целочисленных и вещественных типов данных позволяют оптимизировать использование памяти и производительность, а также поддерживать различные диапазоны значений.

3. Символьная переменная хранит единичный символ, тогда как строковая переменная хранит последовательность символов.

4. Логические переменные хранят значения истинности: true (истина) или false (ложь). Обычно они занимают 1 байт памяти, но могут занимать меньше в зависимости от языка и реализации.

5. Приоритет операций определяет порядок выполнения операций в выражениях. Это нужно для правильного вычисления значений.

6. Операции с одинаковым приоритетом выполняются в порядке их появления в выражении, если не используются скобки.

7. Скобки в выражениях используются для явного указания порядка выполнения операций и могут изменять стандартный приоритет.

8. Если в выражение входят переменные разных типов, то происходит приведение типов, и результатом будет тип, поддерживающий все представленные значения.

9. Операция div возвращает целую часть от деления, а mod — остаток от деления. Эти операции не определены для вещественных чисел, так как они работают только с целыми.

10. Проблема вычисления остатка связана с различиями в реализации операций в разных языках программирования. Следует учитывать разные правила округления и результат.

11. Операция возведения в степень выполняется с помощью умножения основания само на себя нужное количество раз или с использованием специальных функций.

12. Стандартные математические функции включают: sin, cos, tan, exp, log и др. Аргумент тригонометрических функций задается в радианах.

13. Округление до ближайшего целого может выполняться с помощью функции округления, если таковая предусмотрена в языке.

14. Случайные числа — это числа, которые не следуют никакому закономерному порядку. Они нужны для моделирования, игр и статистических выборок.

15. «Естественные» случайные числа могут быть получены из физических процессов, но в цифровой технике они почти не используются из-за невозможности их надежного воспроизводства.

16. Псевдослучайные числа генерируются алгоритмами и повторяются при одинаковых исходных условиях, в отличие от настоящих случайных чисел.

17. Известные функции для получения псевдослучайных чисел: rand(), random(), srand() и др. В зависимости от языка могут быть разные реализации генератора.

# Задание

1. Диапазон значений для вещественных типов данных может сильно различаться в зависимости от языка программирования и архитектуры. Например, в языке Си диапазон для типа float обычно составляет от -3.4E+38 до 3.4E+38, а для double — от -1.7E+308 до 1.7E+308.

2. Программа для нахождения суммы, произведения и среднего арифметического трех целых чисел на Паскале:

```pascal
program Calculate;
var
  a, b, c: integer;
  sum, product, average: real;
begin
  writeln('Введите три целых числа:');
  readln(a, b, c);
  
  sum := a + b + c;
  product := a * b * c;
  average := sum / 3;

  writeln(a, ' + ', b, ' + ', c, ' = ', sum:0:0);
  writeln(a, ' * ', b, ' * ', c, ' = ', product:0:0);
  writeln('Среднее арифметическое = ', average:0:6);
end.

``` 

3. Программа для вычисления площади круга и длины окружности:

```pascal
program CircleCalculator;
const
  Pi = 3.14159265359;
var
  radius: real;
  area, circumference: real;
begin
  writeln('Введите радиус круга:');
  readln(radius);
  
  area := Pi * radius * radius;
  circumference := 2 * Pi * radius;

  writeln('Площадь круга: ', area:0:2);
  writeln('Длина окружности: ', circumference:0:2);
end.
```

4. Программа, которая меняет местами значения двух переменных:


```pascal
program SwapVariables;
var
  x, y, temp: integer;
begin
  writeln('Введите два целых числа:');
  readln(x, y);
  
  temp := x;
  x := y;
  y := temp;

  writeln('После обмена: x = ', x, ', y = ', y);
end.
```

5. Решение для обмена значениями без дополнительных переменных:


```pascal
program SwapWithoutTemp;
var
  x, y: integer;
begin
  writeln('Введите два целых числа:');
  readln(x, y);
  
  x := x + y;
  y := x - y;
  x := x - y;

  writeln('После обмена: x = ', x, ', y = ', y);
end.
```

6. Программа, чтобы возвести число в степень 10:


```pascal
program PowerOfTen;
var
  x, i, result: integer;
begin
  writeln('Введите число:');
  readln(x);
  
  result := 1;
  for i := 1 to 10 do
    result := result * x;

  writeln(x, ' в степени 10 = ', result);
end.
```

При вводе большого числа, например, 78, может возникнуть переполнение, так как результат превысит максимально допустимое значение для целого типа.

7. Вычисления для вещественной переменной с a=2 и b=3:
```pascal
var
  a, b, c: real;
begin
  a := 2;
  b := 3;

  c := a + 1/3; // а
  writeln(c); 

  c := a + 4/2*3 + 6; // б
  writeln(c); 

  c := (a + 4)/2*3; // в
  writeln(c); 

  c := (a + 4)/(b + 3) * a; // г
  writeln(c); 
end.
```

8. Вычисление значения целочисленной переменной с a=26 и b=6:
```pascal
var
  a, b, c: integer;
begin
  a := 26;
  b := 6;

  c := (a mod b) + b; // a)
  writeln(c); 

  c := (a div b) + a; // b)
  writeln(c); 

  // Другие выражения можно добавить аналогично
end.
```

9. Для вычислений с a=-22 и b=-4 результаты могут отличаться в зависимости от обработки отрицательных чисел в разных языках. В Паскале операции div и mod могут дать неожиданные результаты.

10. Программа для разбивки трехзначного числа на цифры:

```pascal
program SplitNumber;
var
  num, hundreds, tens, units: integer;
begin
  writeln('Введите трехзначное число:');
  readln(num);
  
  hundreds := num div 100;
  tens := (num div 10) mod 10;
  units := num mod 10;

  writeln(hundreds, ',', tens, ',', units);
end.
```

11. Программа для вычисления расстояния между двумя точками на числовой оси:

```pascal
program DistanceBetweenPoints;
var
  point1, point2, distance: integer;
begin
  writeln('Введите координаты двух точек:');
  readln(point1, point2);

  if point1 > point2 then
    distance := point1 - point2
  else
    distance := point2 - point1;

  writeln('Расстояние между точками: ', distance);
end.
```

12. Программа для вычисления произведения двух вещественных чисел:

```pascal
program MultiplyRealNumbers;
var
  x, y, result: real;
begin
  writeln('Введите два вещественных числа:');
  readln(x, y);
  
  result := x * y;
  writeln('Произведение: ', result:0:2);
end.
```

13. Программа для округления вещественного числа:

```pascal
program RoundNumber;
var
  number: real;
writeln('Введите вещественное число:');
  readln(number);
  
  writeln('Округленное число: ', round(number));
end.
```

14. Программа для вывода 5 случайных целых чисел на отрезке a, b:

```pascal
program RandomNumbers;
var
  a, b, i, randomNum: integer;
begin
  writeln('Введите два целых числа (a < b):');
  readln(a, b);
  
  Randomize;
  for i := 1 to 5 do
  begin
    randomNum := Random(b - a + 1) + a;
    writeln(randomNum);
  end;
end.
```

15. Программа для моделирования бросания двух кубиков:

```pascal
program DiceRoll;
var
  dice1, dice2, sum: integer;
begin
  Randomize;
  dice1 := Random(6) + 1; // Кубик 1
  dice2 := Random(6) + 1; // Кубик 2
  sum := dice1 + dice2;

  writeln('Сумма кубиков: ', sum);
end.
```
16. Программа для случайного выбора дежурных:

```pascal

program RandomDuties;
var
  N, student1, student2: integer;
begin
  writeln('Введите количество учеников в классе (N):');
  readln(N);

  if N < 2 then
  begin
    writeln('Количество учеников должно быть не менее 2.');
    exit;
  end;

  Randomize;
  
  student1 := Random(N) + 1; // Случайное число от 1 до N
  student2 := Random(N) + 1; // Случайное число от 1 до N

  while student2 = student1 do // Убедимся, что дежурные разные
    student2 := Random(N) + 1;

  writeln('Дежурные: ', student1, ' и ', student2);
end.
```

Проблема: Возможная проблема заключается в том, что два случайных числа могут совпадать, поэтому необходимо убедиться, что дежурные не являются одинаковыми.

17. Программа для генерации случайных вещественных чисел в полуинтервале [а, b):
```pascal
program RandomRealNumbers;
var
  a, b, randomReal: real;
  i: integer;
begin
  writeln('Введите два вещественных числа (a < b):');
  readln(a, b);

  if a >= b then
  begin
    writeln('Ошибка: a должно быть меньше b.');
    exit;
  end; 

  Randomize;
  for i := 1 to 5 do
  begin
    randomReal := a + Random * (b - a); // Генерация случайного вещественного числа в [a, b)
    writeln('Случайное вещественное число ', i, ': ', randomReal:0:2);
  end;
end.
```
