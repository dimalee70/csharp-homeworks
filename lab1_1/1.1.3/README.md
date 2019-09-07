## Задача 3. Приветствуем пользователя и узнаем его возраст

### Описание
Добавим приветствие пользователя. Попросим ввести имя и возраст, выведем привествие и информацию о возрасте.

### Функционал программы

1. Вывод сообщения в консоли **_"Введите ваше имя"._**.
2. Чтение значений и сохранение его в переменную.
3. Вывод сообщения в консоли **_"Введите ваш возраст"._**.
4. Чтение значений и сохранение его в переменную.
5. Вывод приветствия и информацию о возрасте на экран в формате `Привет, {имя}. Ваш возраст: {возраст}`, например `Привет, Админ. Ваш возраст: 18`. 

### Пример

Пример 1
```
Введите ваше имя:
Аноним

Введите ваш возраст:
18

Привет, Админ. 
Ваш возраст: 18.
```

### Реализация
1. Создадим проект или новый repl на сайте [repl.it](https://repl.it/repls) и зададим название `lab1_1_3` (ниже подробная инструкция).

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
  public static void main(String[] args) {
    System.out.println("Hello world!"); //Код сюда
  }
```

3. Для вывода сообщений в консоль используется метод `Console.WriteLine`. Выведем первое сообщение **_"Введите ваше имя":_**

```
Console.WriteLine(Введите ваше имя");
```

4. Чтобы читать сообщения из консоли, воспользуемся специальным методом `Console.ReadLine()` (на следующих лекциях
мы подробнее познакомимся с термином метод).

```
Console.ReadLine();
``` 

5. Чтобы прочитать введенное имя, воспользуемся вызовом чтения строки из консоли:

```
Console.ReadLine();
```
6. Чтобы введенное имя сохранить в переменне, приравняет метод `Console.ReadLine();` в строчковую переменную:

```
 string name = Console.ReadLine();
```

7. Для вывода сообщений в консоль используется метод `Console.WriteLine`. Выведем второе сообщение **_"Введите ваш возраст":_**

```
Console.WriteLine("Введите ваш возраст");
```

8. Чтобы читать сообщения из консоли, воспользуемся специальным методом `Console.ReadLine()` (на следующих лекциях
мы подробнее познакомимся с термином метод).

```
Console.ReadLine();
``` 

9. Чтобы прочитать введенное возраст, в виде строки, воспользуемся вызовом чтения строки из консоли:

```
Console.ReadLine();
```

10. Чтобы прочитать введенный возраст в виде числа, воспользуемся вызовом преобразования строки  в число `Convert.ToInt32()` и в круглых скобках впишите строку, которую будите преобразовывать:

```
Convert.ToInt32("18");
```
11. Чтобы введенное имя сохранить в переменной, вида числа (int), приравняет метод `Console.ReadLine();` в числовую переменную, использую метод преобразования `Convert.ToInt32()`:

```
int age = Convert.ToInt32(Console.ReadLine());
```

7. Для вывода имени в консоли, используйте метод `Console.WriteLine();`, для перевода на новую линию, используйте строчковой литерал `\n`

```
Console.WriteLine($"Привет, {name}.\nВаш возраст: {age}.");
```

8. Завершение работы программы.


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