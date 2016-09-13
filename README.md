# Описание

Это модуль для Битрикс. Модуль позволяет импортировать данные по товарам и разделам из XML выгрузок в формате YML в определённый инфоблок.
Возможно производить импорт в двух режимах:
* Полный импорт всех данных по товарам и разделам. В этом режиме создаются разделы каталога; свойства инфоблока для хранения параметров товаров; добавляются товары с ценами и остатками.
* Импорт только цен и остатков. В этом режиме пропускается создание разделов и свойств товаров; товары не добавляются. Происходит только обновление цен и остатков тех товаров ыгрузки, которые уже есть на сайте.

# Автор модуля

Этот репозиторий является форком репозитория https://github.com/BedrosovaYulia/bitrix_yml_import.git Все права на исходный код принадлежат её автору.

# Изменения в этом форке

* Оформление кода приближено к рекомендациям PSR-2.
* Реализован режим генерации отдельных свойств инфоблока для хранения параметров товаров. Создаются свойства двух типов: либо числовой, либо списочный. В списочный тип заносятся все встреченные в файле импорта варианты свойства товара.
* Реализован функционал импорта остатков товаров по складам.
* Добавлены настройки для профиля импорта:

 -  Переключатель "Все свойства товара добавлять в одно свойство" либо "Каждое свойство товара хранится отдельно"
 -  "Код свойства для всех характеристик"
 -  "Префикс для импортируемых свойств"
 -  "Склады, в которые подгружать остатки"

# Минимальные требования

* PHP 5.5
* Битрикс 15.5
