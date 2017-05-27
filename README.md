Курс Функционального программирования в МФТИ.

Лектор: Сошников Дмитрий.

Семинарист: Лаптев Андрей.

## 1 лабароторная
# Задание 1
Составить программу на функциональном языке, которая печатает таблицу значений элементарной функции, вычисленной двумя способами: по формуле Тейлора и с помощью встроенных функций языка программирования. В качестве аргументов таблицы взять точки разбиения отрезка [a,b] на n равных частей (n + 1 точка, включая концы отрезка), находящихся в рекомендованной области хорошей точности формулы Тейлора. 
Вычисления по формуле Тейлора проводить двумя способами: по экономной в сложностном смысле схеме (с сохранением и домножением предыдущего слагаемого) и «в лоб» вычислением n-го коэффициента. Число слагаемых ряда определяется достижением заданной точности вычислений.
Результат должен быть напечатан в виде таблицы примерно следующего вида:

|x    |Первый способ|Кол-во итераций|Второй способ|Кол-во итераций|Значение функции|
|-----|-------------|---------------|-------------|---------------|----------------|
|0.00	|...          |               |0.0          |...            |                |
|0.05 |||0.0008|...||
|...|...||...|...||
|0.50|...||...|...||

# Задание 2
Составить программу на функциональном языке для решения трансцендентных алгебраических уравнений различными численными методами (итераций, Ньютона и половинного деления). Нелинейные уравнения оформить как параметры-функции, разрешив относительно неизвестной величины в случае необходимости. Применить каждую процедуру к решению трех уравнений, заданных тремя строками таблицы, начиная с варианта с заданным номером. Каждое уравнение решать всеми применимыми методами.
Варианты задания содержатся в таблице 2. Ну и, разумеется, нужно подститать количество итераций для каждого метода.

# Примечание
Для того, чтобы удобно посчитать количество итераций, я ввёл тип Result. Ваши функции должны возвращать именно этот тип. На самом деле, он всего лишь кортеж, где первое значение - результат ваших вычислений, а второе - кол-во итераций.
Можете воспользоваться болванкой, я отметил примерную структуру вашей программы и написал функции printTaylor и printSolve, которые выводят результат, и которые вы должны улучшить.

Помните про то, что языки строгие, поэтому используйте приведение типов 
(так как негоже использовать числа с плавающей точкой там, где нужны только целые)
Для F# это будет [float](https://msdn.microsoft.com/en-us/library/dd233220.aspx) (ну и не забывать расставлять точки), 
для Haskell - [fromIntegral](http://learnyouahaskell.com/types-and-typeclasses)

