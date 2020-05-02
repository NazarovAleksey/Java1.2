# Отчёт о тестировании Credit Card Number Validator

## Краткое описание

C 01.05.2020 по 02.05.2020 было проведено инсталяционное тестирование IntelliJ IDEA и функциональное тестирование приложения Credit Card Number Validator.

На тестирование затрачено: 3 часа

В результате тестирования выявлены следующие дефекты:
* [Руководство по установке IntelliJ IDEA. Не рабочая ссылка, шаг 19](https://github.com/NazarovAleksey/Java1.2/issues/1)
* [Credit Card Number Validator. Проверка валидного 13 значного номера карты.](https://github.com/NazarovAleksey/Java1.2/issues/2)
* [Credit Card Number Validator. Проверка валидного 15 значного номера карты.](https://github.com/NazarovAleksey/Java1.2/issues/3)
* [Credit Card Number Validator. Проверка валидного 17 значного номера карты.](https://github.com/NazarovAleksey/Java1.2/issues/4)
* [Credit Card Number Validator. Проверка валидного 18 значного номера карты.](https://github.com/NazarovAleksey/Java1.2/issues/5)
* [Credit Card Number Validator. Проверка валидного 19 значного номера карты.](https://github.com/NazarovAleksey/Java1.2/issues/6)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* [Руководство по установке IntelliJ IDEA](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/idea.md)
* [Программный код Credit Card Number Validator](https://github.com/NazarovAleksey/Java1.2/blob/master/src/Main.java)

В качестве тестовых данных использовались данные сайтов [names.igopaygo.com](https://names.igopaygo.com/ru/%D0%9A%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D1%8B%D0%B5-%D0%BA%D0%B0%D1%80%D1%82%D1%8B) и [freeformatter.com](https://www.freeformatter.com/credit-card-number-generator-validator.html#fakeNumbers):

VISA:
* 4539950107964007 - Result is OK
* 4323050109106616105 - Result is FAIL

Visa Electron:
* 4026845347167199 - Result is OK
* 4508503364914483 - Result is OK

MasterCard:
* 2720994169333183 - Result is OK
* 5452740409361394 - Result is OK

Maestro:
* 6759492697111531 - Result is OK
* 0604188732018752 - Result is OK

Произвольные данные:
* Номер карты не заполнен - Result is FAIL
* Номер карты равен одному символу (4) - Result is FAIL
* Номер карты равен 6 символов (472529) - Result is FAIL
* Номер карты равен 13 символам (4024007106335) - Result is FAIL
* Номер карты равен 15 символов (210028858591578) - Result is FAIL
* Номер карты равен 16 символам (5314509173114224) - Result is OK
* Номер карты равен 17 символам (67092149532982363) - Result is FAIL
* Номер карты равен 18 символов (586824160825533338) - Result is FAIL
* Номер карты равен 19 символов (4716957671546798339) - Result is FAIL
* Номер карты равен 20 символов (47169576715467983391) - Result is FAIL

Тестирование производилось в следующем окружении:
* Windows 10 64x
* Java 11.0.7+10
* IntelliJ IDEA 2020.1.1 (Community Edition)