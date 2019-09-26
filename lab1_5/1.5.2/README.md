# Домашнее задание к занятию 5. Массивы многомерные
## Задача 1. Поворот матрицы на 90 градусов по часовой стрелке

### Описание
Научимся поворачивать матрицу с равными сторонами. Этот алгоритм мог бы быть использован в графических редакторах 
вроде Photoshop для поворота изображений.

Дано: двумерная матрица 8 на 8 из случайных чисел от 0 до 255 (спектр цветов GrayScale).
Напишите алгоритм "поворота" такой матрицы на 90 градусов по часовой стрелке.

### Функционал программы
1. Создание матрицы в программе;
2. Вывод матрицы до поворота;
3. Разворот матрицы;
4. Вывод матрицы после поворота на 90 градусов.

### Пример
Дана следующая матрица:
``` 
114 112 148  83 204  22 125  31
192 231 245 128  63 246 139  17
 61 128 224  45  91  57 239  34
219 237 167 191 236 146 144 117
 35 199 102 124 208 195  21 147
 52 229 126  32  24 145  19  39
107  43 190  43  47 172  18  19
 62 221   6 208 241 198 187  85
```  
Вывод:
```  
 62 107  52  35 219  61 192 114
221  43 229 199 237 128 231 112
  6 190 126 102 167 224 245 148
208  43  32 124 191  45 128  83
241  47  24 208 236  91  63 204
198 172 145 195 146  57 246  22
187  18  19  21 144 239 139 125
 85  19  39 147 117  34  17  31
```  

### Пример реализации
1. Итак, у нас есть матрица с размерами 8x8, которую нужно повернуть на 90 градусов по часовой стрелке.
Для начала создадим матрицу (размерность матрицы сохраним в переменной filedSize).
    ```
      int SIZE = 8;
      int[,] colors = new int[SIZE,SIZE];
    ```  
2. Теперь заполним матрицу случайными значениями в диапазоне от 0 до 255:
    ```java
      Random random = new Random();
      for (int i = 0; i< SIZE; i++) {
        for (int j = 0; j< SIZE; j++) {
        // для случайных значений воспользуемся готовым решением из библиотеки java.util.Random
          colors[i][j] = random.Next(256);
        }
      }
    ```  
3. Выводим матрицу на экран:
    ```
      for (int i = 0; i< SIZE; i++) {
        for (int j = 0; j< SIZE; j++) {
          // %4d означает, что мы под каждый номер резервируем 4 знака
          // (незанятые будут заполнены пробелами)
          // таким образом, у нас получится ровная таблица
          System.Console.Write(colors[i,j]+"\t");
        }
        // Переход на следующую строку
        System.Console.WriteLine();
      }
    ```  
4. Для повернутой матрицы создадим пустой массив той же размерности:
    ```
      int[][] rotatedColors = new int[SIZE][SIZE];
    ``` 
5. Новая матрица должна принять значения ячеек первой матрицы, но с поворотом на 90 градусов по часовой стрелке.
Это значит, что значение первой ячейки rotatedColors[0][0] (первая строка, первое значение) новой матрицы
должно быть равно первому значению ячейки последней строки матрицы colors (colors[SIZE-1][0]).
6. Исходя из вышесказанного нужно: 
  * написать циклы, при помощи которых можно пробежаться по матрицам,
  * каждому элементу новой матрицы rotatedColors присвоить соответствующее значение из имеющейся colors матрицы.

Перебор элементов матрицы можно организовать встроенными циклами так же, как вы вывели значения на экран colors матрицы.

### Задача 1*. Поворот матрицы на 90/180/270 градусов
Добавьте в задачу \#1 возможность вводить угол поворота (кратный 90) с клавиатуры.

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