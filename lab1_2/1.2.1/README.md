## Задача 1. Високосный год

### Описание
Нужно написать программу, которая будет рассчитывать количество дней в году.
Зачем это бывает нужно? Варианты бывают разные: например, для расчета продолжительности долгосрочных проектов в днях или чтобы
узнать, сколько дней потребуется для космической экспедиции на Марс.
Для расчета количества дней в году требуется знать несколько правил:
- В високосном году 366 дней, в обычном 365.
- Високосный год — это год, номер которого делится без остатка на 400 (например 2000 или 2400), либо делится на 4 но не делится на 100 (например 2008, 2096, но не 2100).

### Функционал программы
1. Вывод сообщения в консоли `Введите год в формате "yyyy"`.
2. Ввод года в формате `yyyy` (например 2004).
3. Чтение значения из консоли и расчет количества дней.
4. Результат работы программы: напечатать в консоли количество дней в году `Количество дней 365` или `Количество дней 366`.

### Пример
Пример 1
```
Введите год в формате "yyyy"
2000 <нажмите enter>
Количество дней 366
```
Пример 2
```
Введите год в формате "yyyy"
2018 <нажмите enter>
Количество дней 365
```

### Реализация
1. Создадим проект или новый repl на сайте [repl.it](https://repl.it/repls) и зададим название `lab1_1_2` (ниже подробная инструкция).

2. В файле `Program.cs` или `main.cs` написан следующий код:

```
using System;

class MainClass {
  public static void Main (string[] args) {
    Console.WriteLine ("Hello World");
  }
}
``` 

Весь код выполнения задачи нужно писать вместо `Console.WriteLine ("Hello World");`:

```
   public static void Main (string[] args) {
    Console.WriteLine ("Hello World");//Код сюда
  }
```
3. Для вывода сообщений в консоль используется метод `Console.WriteLine`.
```
Console.WriteLine("Измените сообщение для вывода его в консоли");
```
4. Чтобы читать сообщения из консоли, воспользуемся специальным методом `Console.ReadLine()` (на следующих лекциях
мы подробнее познакомимся с термином метод).

```
Console.ReadLine();
``` 

5. Чтобы прочитать введенное возраст, в виде строки, воспользуемся вызовом чтения строки из консоли:

```
Console.ReadLine();
```

6. Чтобы прочитать введенный год в виде числа, воспользуемся вызовом преобразования строки  в число `Convert.ToInt32()` и в круглых скобках впишите строку, которую будите преобразовывать:

```
Convert.ToInt32("2018");
```

7. Как проверить, високосный ли год? 
Для этого сначала надо проверить делимость на 400, используя `year % 400 == 0`. Специальный оператор `%` - возвращает остаток от деления. Результат вычисления будет равен 0, только если число делится нацело, иначе вернется остаток от деления.
Если год делится на 400 без остатка, значит в нем точно 366 дней. Если нет, то — аналогично проверить делимость на 100: если год делится на 100, то в нем точно 365 дней. И наконец, если год не делится ни на 400, ни на 100, то проверяем делимость на 4: если делится, — то — 366 дней, иначе — 365.

8. Чтобы последовательно проверить делимость введенного числа, нужно воспользоваться тернарным оператором и запишите ответ в строчковую переменную `Выражение1 ? Выражение2 : ВыражениеЗ;`.

```
string answer = ((10%2) == 0)? "Четное": "Нечетное";
```
9. Вывести ответ.
10. Завершение работы программы.

## Инструкция по выполнению домашнего задания

- Первый вариант

1. Зарегистрируйтесь на сайте <a href="http://repl.it/" target="_blank">Repl.IT</a>.
2. Перейдите в раздел **my repls**.
3. Нажмите кнопку **Start coding now!**, если приступаете впервые, или **New Repl**, если у вас уже есть работы.
4. В списке языков выберите `C#`.
5. В поле название repl напишите номер задачи, например: `lab1_1_1`.
6. Код пишите в левой части окна вместо строки `Console.WriteLine ("Hello World");;`.
7. Посмотреть результат выполнения файла можно, нажав на кнопку **Run**. Результат появится в правой части окна.
8. После окончания работы нажмите кнопку **Share** и скопируйте ссылку из поля Share link.
9. В классе на сайте <a href="https://classroom.google.com/c/MjM5MzEwOTA3NTJa" target="_blank">classroom.google</a> в поле комментария к домашней работе вставьте скопированную ссылку и отправьте работу на проверку.

*Никаких файлов прикреплять не нужно.*

- Второй вариант

1. Создайте папку с названием лабораторной работы, например: `lab1_1_1`.
2. Откройте программу VisualStudio Code.
3. Откройте, созданную вами папку в VisualStudio Code.
3. Создайте проект при помощи командной строки командой 
`$ dotnet new console`.
4. Откройте файл `Program.cs` в текстовом редакторе.
5. Код пишите в правом окне вместо строки `Console.WriteLine ("Hello World");;`.
6. Посмотреть результат выполнения файла можно, написав команду `$ dotnet run`. Результат появится в нижней части окна.
7. После окончания работы заархивируйте папку с название лабораторной работы в zip архив.
8. В классе на сайте <a href="https://classroom.google.com/c/MjM5MzEwOTA3NTJa" target="_blank">classroom.google</a> в поле комментария к домашней работе вставьте zip архив проекта и отправьте работу на проверку.

*Для подробной информации перейдите по <a href="https://docs.microsoft.com/ru-ru/dotnet/core/tutorials/with-visual-studio-code" target="_blank">ссылке</a>.*