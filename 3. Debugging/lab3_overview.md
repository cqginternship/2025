### Искусство отладки
# Лабораторная работа N 3
### Задание к выполнению лабораторной работы.

В программе есть несколько багов разной природы.  
Для поиска багов проверьте следующие сценарии в диагностическом режиме.

#### Поиск городов по имени

Обратите внимание, что Geo-сервис должен поддерживать поиск на местном и на английском языках.

---

Пример:
```
$ ./build/geo --debug --config ./geo-config.json --name München
```
Ожидаемый результат: München

---

Пример:
```
$ ./build/geo --debug --config ./geo-config.json --name Zelenograd
```
Ожидаемый результат: Зеленоград

#### Поиск городов по координатам

Пример:
```
./build/geo --debug --config ./geo-config.json --lat 22.563887 --lon 88.345477
```
Ожидаемый результат: Kolkata

#### Поиск регионов с учетом фильтра

Пример:
```
$ ./build/geo --debug --config ./geo-config.json --dist 50 --lat 56 --lon 37 --filter 1
```
Ожидаемый результат: Москва и Московская область

---

Пример:
```
$ ./build/geo --debug o --debug --config ./geo-config.json --dist 50 --lat 44.183183 --lon 42.199114 --filter 2
```
Ожидаемый результат: Ставропольский край и Карачаево-Черкесия

---

Пример:
```
$ ./build/geo --debug o --debug --config ./geo-config.json --dist 25 --lat 41.116525 --lon 1.257839 --filter 4
```
Ожидаемый результат: Catalunya

---

Пример:
```
$ ./build/geo --debug --config ./geo-config.json --dist 20 --lat 38.730065 --lon 33.358818 --filter 8
```
Ожидаемый результат: Aksaray, Konya, Ankara

---

Пример:
```
$ ./build/geo --debug o --debug --config ./geo-config.json --dist 10 --lat 42.057485 --lon 48.288689 --filter 11
```
Ожидаемый результат: Дагестан
