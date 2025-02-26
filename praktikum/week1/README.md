# Intro to C++

## Псевдоними - referances

- алтернативно име на променлива
- директен достъп до оригиналната променлива
- не могат да се променят след инициализация
- когато се подават като аргумент на функция не се прави копие на променливата (директно я достъпваме в тялото)
- не се заделя памет за тях
- могат да са const (да направим променлива read-only във функция например)

```c
int a = 5;
int& b = a;
b = 6;
// a = 6
```

## Памет

- new и delete
- когато е масив delete[]

```c
int* arr = new int[10];
delete[] arr;
```

## Errors

```c
try {
    throw std::runtime_error("Error occurred!");
} catch (const std::exception& e) {
    std::cout << e.what() << std::endl;
}
```

## Default стойности на аргументите

```c
int sum(int a = 0, int b = 0){
return a + b;
}
```

# Малко за стрктурите.

Какво е структура:
Това е тип създаден от нас съдържащ в себе си други типове създадени от нас или базови типове(int, float, char\* и т.н.).

Синтаксис
struct <име> {
<тип на параметър> <име на параметър>;
...
};
Може да вземем стойноста от една структура, като направим нейна истанция по следня начин, като ползваме оператора '.'

```c
struct s {
  int n;
  double b;
};

struct s t1 = {1, 2};

printf("%d", t1.n); // извежда на екрана 1
```

# Задача 1 (Платформа за менежиране на студенти)

Трябва да дефинирате структура, в която да пазите

- ФН номер на студента от новия формат (xMI0x00xxx)
- име
- възраст
- среден успех

Функция която създава студенти по параметри и връща новосъздадения студент.

Функция която принтира информацията за студента в приличен външен вид.

Функция, която казва дали средния успех на студента е 2 <= x < 3

Функция, която по масив от студенти с максимален размер 10, връща средния успех. Като параметри функцията трябва да приема брой студенти в масива и самия масив и да връща `double` среден успех.

# Задача 2 (Сортиране на играчи)

Имате структура от данни за отбори на тенис на маса за двама те имат полета за име на отбор, за брой точки и за идентификационен номер на играчите (Идентификационния номер е число). Напишете функция `print_leaderboard`, която приема списък с играчи на тенис на маса и им извежда имената на отборите и брой точки сортирани от отбора с най-много точки до отбора с най-малко точки.
