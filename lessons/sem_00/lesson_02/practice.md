# Структура языка. Логический тип данных. Практическое занятие

Рашения и ответы на вопросы отправьте с помощью [формы](https://forms.yandex.ru/u/66c9ec8d50569050dea17873/).

## Задание 1. Чтение и печать

В листингах кода мы часто использовали встроенную функцию `print()`. Функция `print()` используется для вывода каких-либо сообщений в стандартный поток вывода. В Python также существует возможность читать какие-либо данные из стандартного потока ввода. Для этих целей существует встроенная функция `input()`. `input()` читает поток символов из стандратного потока ввода до тех пор, пока не встретится символ конца строки (пользователь нажимает ENTER). Результат выполнения - считанный поток символов.

В данном задании предлагается попрактиковаться в работе с описанными функциями.

**Задачи**:
- Исследуйте функции `print()` и `input()` с помощью встроенной функции `help()`, которая позволяет получить справочную информацию о переданном объекте.
- Поэкспериментируйте с параметрами функций. Как они влияют на результат выполнения?
- Прочитайте любые данные из стандартного потока ввода и сохраните их в переменную.
- Определите тип данных объекта, на который ссылается ваша переменная. Выведите этот тип данных в стандартный поток вывода. Что это за тип данных?
- Прочитайте последовательность символов, состоящую только из цифр от 0 до 9 и запишите ее в новую переменную. Какого типа данных объект, на который ссылается новая переменная?
- Какие выводы можно сделать исходя из полученных результатов?

## Задание 2. Составное присваивание

Объекты логического типа данных поддерживают использование составного присваивания. Составное присваивание - это присваивание, состоящее из двух частей: выполнения какой-либо операции и привязки полученного результата к переменной, расположенной слева от оператора. Приведем пример:

```python
flag = True
flag &= True
```

В примере выше мы создали переменную `flag` с булевым значением `True`, а затем вычислили битовое И между `flag` и булевым значением `True`. Результат выполнения второй строки соответствует результату выполнения:
```python
flag = flag & True
```

Важно, что в отличие от простого присваивания, составное присваивание не создает новых переменных и может использоваться только с существующими переменными. Поэтому первая строка с привязкой переменной `flag` существенна.

**Задачи**
- Проверьте, что будет, если убрать первую строку в приведенном выше листинге кода. Какой результат будет получен?
- Верните первую строку, выполните код. Распечатайте переменную `flag`. Чему равно значение переменной `flag` после выполнения кода?
- В теоретической части мы говорили, что логический тип данных является неизменяемым. Но в приведенном примере с помощью оператора составного присваивания мы изменили значение переменной `flag`. Нет ли здесь противоречия? Как это можно объяснить? Аргументируйте свою позицию.

## Задание 3. else и continue

В теоретической части мы говорили, что блок `else` цикла `while` будет выполнен только в том случае, если цикл был завершен не после выполнения инструкции `break`. А будет ли выполнен блок `else`, если в процессе выполнения цикла `while` будет выполнена инструкция `continue`?

## Задание 4. do while

Цикл `while` выполняется достаточно прямолинейно: сначала мы проверяем условие цикла, если условие ложно - завершаем работу, если условие истинно - выполняем тело цикла и уходим на следующую итерацию. В большинстве случаев такого подхода достаточно. Однако в некоторых случаях нам необходимо сначала выполнить итерацию, и только потом проверить условие. Такой цикл называется `do while` и является встроенной частью некоторых языков программирования. Однако в Python цикла `do while` нет, но поведение, которое он позволяет реализовать, иногда является очень нужным. Подумайте, как можно было бы реализовать цикл `do while` при помощи цикла `while`? Ответ запишите в виде псевдокода Python.