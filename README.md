<h1 align="center">Домашнее задание к работе 6(Индивидуальный проект)</h1>
<div align="center">



## Условие задачи

<img width="655" height="46" alt="изображение" src="https://github.com/user-attachments/assets/f7c88308-d56f-4cf2-97c7-34ff9c731af8" />



## 1. Алгоритм и блок-схема

<div align="center">

### Алгоритм
1. **Начало**
2. Ввод числа N с клавиатуры <br>
   - `N` (N<1000)
3. Создание переменной для модуля N
   - `int fabsN = fabs(N)`
4. Создание счетчика цифр<br>
   - `C`
5. Начало цикла.
6. Результат, если N меньше 10 по модулю
7. Результат, если N от 10 до 100 по модулю
8. Результат, если N от 100 до 1000 по модулю
9. Результат, если N больше 1000 по модулю
10. Конец цикла
12. **Конец**

</div>

### Блок-схема

<img width="2011" height="1652" alt="LAB_6_3a" src="https://github.com/user-attachments/assets/f9a98483-632c-4c1f-9558-97770a7f5ca3" />



</div>

## 2. Реализация программы

```c
// Подключение нужных библиотек
#include <stdio.h>
#include <locale.h>
#include <math.h>

// Создание основной функции
int main() {
    // Добавление русской локали
    setlocale(LC_CTYPE, "RUS");
    // Создание переменной под число N и счетчик
    int N;
    int C;
    // Создание ввода числа N из терминала
    puts("Введите число N (N < 1000): ");
    scanf_s("%d", &N);
    getchar();

    // Создание переменной под модуль числа
    int fabsN = fabs(N);
    // Проверка на число из одной цифры
    if (fabsN < 10) {
        puts("Ваше число состоит из одной цифры, оно не может дать двухзначное число при сложении цифр!");
    }
    // Проверка на число из двух цифр
    else if (fabsN < 100) {
        C = (fabsN / 10) + (fabsN % 10);
        if (C >= 10 && C <= 99) {
            printf("Ваше число при сложении цифр дает двухзначное число! \nВаше число - %d\nЧисло при сложении цифр - %d", N, C);
        }
        else {
            printf("Ваше число при сложении цифр не дает двухзначное число! \nВаше число - %d\nЧисло при сложении цифр - %d", N, C);
        }
    }
    // Проверка на число из трех цифр
    else if (fabsN < 1000) {
        int digit1 = fabsN / 100;
        int digit2 = (fabsN / 10) % 10;
        int digit3 = fabsN % 10;
        C = digit1 + digit2 + digit3;

        if (C >= 10 && C <= 99) {
            printf("Ваше число при сложении цифр дает двухзначное число! \nВаше число - %d\nЧисло при сложении цифр - %d", N, C);
        }
        else {
            printf("Ваше число при сложении цифр не дает двухзначное число! \nВаше число - %d\nЧисло при сложении цифр - %d", N, C);
        }
    }
    // Результат если модуль числа больше 1000
    else {
        puts("Число должно быть меньше 1000 по модулю!");
    }
}

```
<div align="center">

## 3. Результаты работы программы
<img width="975" height="505" alt="изображение" src="https://github.com/user-attachments/assets/57b8e656-9517-4a84-a2e5-1fbacaec8eff" />
<img width="979" height="512" alt="изображение" src="https://github.com/user-attachments/assets/fe8fddcf-abf2-475b-b61d-a8eda5afac9a" />
<img width="974" height="511" alt="изображение" src="https://github.com/user-attachments/assets/4c9265a5-aaa0-4cf7-845c-c3fce9062647" />

<h1 align="center">Домашнее задание к работе 6*</h1>
<div align="center">



## Условие задачи

<img width="314" height="207" alt="изображение" src="https://github.com/user-attachments/assets/2a6f644c-01e8-4522-83a1-b986f6a4d1bd" />




## 1. Алгоритм и блок-схема

<div align="center">

### Алгоритм
1. **Начало**
2. Ввод чисел x,y с клавиатуры <br>
   - `x`
   - `y`
3. Проверка принадлежности точки
   - `if (x * x + y * y <= 4 && y >= x && x >= 0)`
4. Вывод результата в зависимости от истинности выражения<br>
5. **Конец**

</div>

### Блок-схема

<img width="882" height="642" alt="LAB_6_3b" src="https://github.com/user-attachments/assets/807be65b-22f2-46f1-a76f-eb66a7ff8548" />




</div>

## 2. Реализация программы

```c
// Подключение нужных библиотек

#include <stdio.h>
#include <locale.h>
#include <math.h>

// Создание основной функции

int main() {
	
	// Добавление русской локали
	
	setlocale(LC_CTYPE, "RUS");
	
	// Добавление переменных x,y для ввода с консоли
	
	float x;
	float y;
	
	// Ввод x,y с консоли
	
	puts("Введите переменные x,y для проверки принадлежности точки к заштрихованной области");
	scanf_s("%f %f", &x, &y);
	getchar();

	// Проверка принадлежности точки
	if (x * x + y * y <= 4 && y >= x && x >= 0)
		printf("Ваша точка входит в заштрихорванную область функции x^2 + y^2 = 4 \nВаша точка(%.2f , %.2f)", x, y);
	else
		printf("Ваша точка не  входит в заштрихованную область функции x^2 + y^2 = 4 \nВаша точка(%.2f , %.2f)", x, y);


		
}
```
<div align="center">

## 3. Результаты работы программы

<img width="969" height="502" alt="изображение" src="https://github.com/user-attachments/assets/41b707b3-f4cb-4ed7-87ae-f36ff7c76d71" />
<img width="975" height="504" alt="изображение" src="https://github.com/user-attachments/assets/8041228d-14f6-452d-9aa9-e6543def9dfa" />






## 4. Информация о разработчике

Выполнил Гребенников Артем, бИПТ-252


