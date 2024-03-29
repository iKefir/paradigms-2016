Тесты к курсу «Парадигмы программирования»
====

[Условия домашних заданий](http://www.kgeorgiy.info/courses/java-intro/homeworks.html)

Домашнее задание 5. Вычисление выражений
---
 * *Базовая*
    * Реализовать интерфейс [Expression](java/expression/Expression.java)
    * [Исходный код тестов](java/expression/ExpressionTest.java)
 * *Простая*
    * Реализовать интерфейс [DoubleExpression](java/expression/DoubleExpression.java)
    * [Исходный код тестов](java/expression/DoubleExpressionTest.java)

Домашнее задание 4. Очередь на связном списке
---
 * *Базовая*
    * [Исходный код тестов](java/queue/QueueTest.java)
    * [Откомпилированные тесты](artifacts/queue/QueueTest.jar)
 * *Простая*
    * Добавить в интерфейс очереди и реализовать метод
      `toArray`, возвращающий массив,
      содержащий элементы, лежащие в очереди в порядке
      от головы к хвосту
    * Исходная очередь должна остаться неизменной
    * Дублирования кода быть не должно
    * [Исходный код тестов](java/queue/QueueToArrayTest.java)
    * [Откомпилированные тесты](artifacts/queue/QueueToArrayTest.jar)
 * *Усложненная*
    * Добавить в интерфейс очереди и реализовать методы
        * `filter(predicate)` – создать очередь, содержащую элементы, удовлетворяющие 
            [предикату](https://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html)
        * `map(function)` – создать очередь, содержащую результаты применения 
            [функции](https://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html)
    * Исходная очередь должна остаться неизменной
    * Тип возвращаемой очереди должен соответствовать типу исходной очереди
    * Взаимный порядок элементов должен сохраняться
    * Дублирования кода быть не должно
    * [Исходный код тестов](java/queue/QueueFunctions.java)
    * [Откомпилированные тесты](artifacts/queue/QueueFunctionsTest.jar)

Домашнее задание 3. Очередь на массиве
---
Модификации
 * *Базовая*
    * [Исходный код тестов](java/queue/ArrayQueueTest.java)
    * [Откомпилированные тесты](artifacts/queue/ArrayQueueTest.jar)
 * *Простая*
    * Реализовать метод `toArray`, возвращающий массив,
      содержащий элементы, лежащие в очереди в порядке
      от головы к хвосту.
    * [Исходный код тестов](java/queue/ArrayQueueToArrayTest.java)
    * [Откомпилированные тесты](artifacts/queue/ArrayQueueToArrayTest.jar)
 * *Усложненная*
    * Реализовать методы
        * `push` – добавить элемент в начало очереди
        * `peek` – вернуть последний элемент в очереди
        * `remove` – удалить последний элемент из очереди 
    * [Исходный код тестов](java/queue/ArrayQueueDequeTest.java)
    * [Откомпилированные тесты](artifacts/queue/ArrayQueueDequeTest.jar)

Домашнее задание 2. Бинарный поиск
----
Модификации
 * *Базовая*
    * [Исходный код тестов](java/search/BinarySearchTest.java)
    * [Откомпилированные тесты](artifacts/search/BinarySearchTest.jar)
 * *Простая*
    * Если в массиве `a` отсутствует элемент, равный `x`, то требуется
      вывести индекс вставки в формате, определенном в 
      [`Arrays.binarySearch`](http://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html#binarySearch-int:A-int-).
    * Класс должен иметь имя `BinarySearchMissing`
    * [Исходный код тестов](java/search/BinarySearchMissingTest.java)
    * [Откомпилированные тесты](artifacts/search/BinarySearchMissingTest.jar)
 * *Усложненная*
    * Требуется вывести два числа: начало и длину диапазона элементов,
      равных `x`. Если таких элементов нет, то следует вывести
      пустой диапазон, у которого левая граница совпадает с местом
      вставки элемента `x`.
    * Не допускается использование типов `long` и `BigInteger`.
    * Класс должен иметь имя `BinarySearchSpan`
    * [Исходный код тестов](java/search/BinarySearchSpanTest.java)
    * [Откомпилированные тесты](artifacts/search/BinarySearchSpanTest.jar)

Домашнее задание 1. Хэширование
----

Модификации
 * *Простая*
    * Класс должен иметь имя `CalcSHA256` и подсчитывать [SHA-256](https://en.wikipedia.org/wiki/Secure_Hash_Algorithm)
    * [Исходный код тестов](java/hash/CalcSHA256Test.java)
    * [Откомпилированные тесты](artifacts/hash/CalcSHA256Test.jar)
 * *Усложненная*
    * Напишите простой аналог утилиты [sha256sum](http://linux.die.net/man/1/sha256sum)
    * Класс должен называться `SHA256Sum`
    * Список файлов для хэширования передается в виде аргументов командной строки
    * Если список файлов пуст, то хэшируется стандартный ввод а именем файла считается `-`
    * Вывод хэшей осуществляется в формате `<хэш> *<имя файла>`
    * [Исходный код тестов](java/hash/SHA256SumTest.java)
    * [Откомпилированные тесты](artifacts/hash/SumSHA256Test.jar)

Для того, чтобы протестировать исходную программу:

 1. Скачайте тесты ([CalcMD5Test.jar](artifacts/hash/CalcMD5Test.jar))
 * Откомпилируйте `CalcMD5.java`
 * Проверьте, что создался `CalcMD5.class`
 * В каталоге, в котором находится `CalcMD5.class` выполните команду 
    ```
       java -jar <путь к CalcMD5Test.jar>
    ```
    * Например, если `CalcMD5Test.jar` находится в текущем каталоге, выполните команду 
    ```
        java -jar CalcMD5Test.jar
    ```
    
Исходный код тестов: 

* [CalcMD5Test.java](java/hash/CalcMD5Test.java), 
* [HashChecker.java](java/hash/HashChecker.java)
