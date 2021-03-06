# Отчёт о тестировании java-приложения KeyValidator

## Краткое описание

25.05.2020 - 26.05.2020 было проведено установочное, дымовое и функциональное тестирование приложения KeyValidator.

На тестирование затрачено: 3 часа

В результате тестирования выявлены следующие дефекты:
* неполное описание шагов в инструкции по установке OpenJDK11 [Issue #1](https://github.com/Boldyrev-M/Javaqa5-1-1/issues/1)
* не предусмотрена реакция программы на вводимые данные, не соответствующие правильному формату: вместо сообщения о неверном формате выдается список ошибок [Issue #3](https://github.com/Boldyrev-M/Javaqa5-1-1/issues/3)
* программа некорректно работает в ряде случаев либо неверно указаны тестовые ключи для проверки [Issue #2](https://github.com/Boldyrev-M/Javaqa5-1-1/issues/2)

## Описание процесса тестирования

В процессе тестирования проверена инструкция по установке OpenJDK11, инструкция по запуску приложения KeyValidator и работа программы на тестовых данных.

В качестве тестовых данных для проверки использовались ключи из [Руководства по использованию KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md)

* Валидные ключи:

| Указанные ключи | Полученный результат | Ожидаемый результат |
| :--- | :---: | :---: |
| 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998 |  OK  |  OK  |
| 80b427f8-92cd-3aae-ba04-3927fbe17c6  | **FAIL** |  OK  |
| b295bc63-9f03-3b4b-af80-969b39f8c262 |  OK  |  OK  |
| 387eedc6-12e9-3b32-9881-63b6b5e85317 | **FAIL** |  OK  |
| c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180 |  OK  |  OK  |

* Невалидные ключи:

| Указанные ключи | Полученный результат | Ожидаемый результат |
| :--- | :---: | :---: |
| 18252235-78e0-44a5-8720-556f0c7da17a | FAIL | FAIL |
| e66075b6-ddad-445e-baf6-161b3289522b | FAIL | FAIL |
| b6d53250-f07e-4352-a293-6102ddf7f1ca | FAIL | FAIL |
| c2bc778a-1cb9-46c6-b435-0489649d2a42 | FAIL | FAIL |
| 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1 |  **OK**  | FAIL |
    
## Тестирование производилось в следующем окружении:

* версия и разрядность ОС:
Windows 10 64-разрядная
Microsoft Windows [Version 10.0.18363.476]

* версия Java:
openjdk version "11.0.7" 2020-04-14
OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.7+10)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.7+10, mixed mode)
