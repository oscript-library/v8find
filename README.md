# v8find

[![Stars](https://img.shields.io/github/stars/khorevaa/v8find.svg?label=Github%20%E2%98%85&a)](https://github.com/khorevaa/v8find/stargazers)
[![Release](https://img.shields.io/github/tag/khorevaa/v8find.svg?label=Last%20release&a)](https://github.com/khorevaa/v8find/releases)
[![Открытый чат проекта https://gitter.im/EvilBeaver/oscript-library](https://badges.gitter.im/khorevaa/v8find.png)](https://gitter.im/EvilBeaver/oscript-library)

[![Build Status](https://travis-ci.org/khorevaa/v8find.svg?branch=master)](https://travis-ci.org/khorevaa/v8find)
[![Coverage Status](https://coveralls.io/repos/github/khorevaa/v8find/badge.svg?branch=master)](https://coveralls.io/github/khorevaa/v8find?branch=master)

# Библиотека для поиска установленных версий платформы 1С

Данная библиотека предназначена для поиска установленных версий платформы 1С в различных каталогах

## Возможности

* Поиск конкретной версии платформы для примера `8.3.13.1513`
* Поиск версии платформы по маске для примера `8.3.13`, `8.3`
* Получение путей к приложениям платформы
    * Приложение - `1cv8`
    * Тонкий клиент - `1cv8c`
    * Утилита `rac`  для администрирования кластера 1С - `rac`
* Получение списка всех установленных версий платформы 1С
* Получение версии платформы с учетом разрядности `x64` или `x86`

## Установка

Для установки необходимо:
* Скачать файл v8find.ospx из раздела [releases](https://github.com/khorevaa/v8find/releases)
* Воспользоваться командой:

```
opm install -f <ПутьКФайлу>
```
или установить с хаба пакетов

```
opm install v8find
```

## Пример работы

* Получение пути к приложению 1С

    ```bsl

        ПутьКПредприятию_x86 = Платформа1С.ПутьКПредприятию("8.3.13.1513", РазрядностьПлатформы.x86);
        ПутьКПредприятию_x64 = Платформа1С.ПутьКПредприятию("8.3.13", РазрядностьПлатформы.x64);
        
    ```

* Получение пути к тонкому клиенту 1С

    ```bsl

        ПутьКТонкомуКлиенту = Платформа1С.ПутьКТонкомуКлиенту("8.3.13");
        ПутьКТонкомуКлиенту = Платформа1С.ПутьКТонкомуКлиенту("8.3");
        
    ```

* Получение пути к утилите `rac`

    ```bsl

        ПутьКRAC = Платформа1С.ПутьКRAC("8.3.13");
        ПутьКRAC = Платформа1С.ПутьКRAC("8.3");
        
    ```

* Получение пути к утилите `dbgs`

    ```bsl

        ПутьКDBGS = Платформа1С.ПутьКDBGS("8.3.13");
        ПутьКDBGS = Платформа1С.ПутьКDBGS("8.3");
        
    ```

## Публичный интерфейс

[Документация публичного интерфейса (в разработке)](docs/README.md)

## Доработка

Доработка проводится по git-flow. Жду ваших PR.

## Лицензия

Смотри файл [`LICENSE`](LICENSE).
