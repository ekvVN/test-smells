## Используется `androidTest` там, можно запустить тест на хосте

### Проблемы
Тесты выполняются долго, требуют настоящего устройства или эмулятора.

### Теория
Robolectric это библиотека, которая позволяет на хост машине выполнять андроидно-специчифичный код.

Robolectric содержит почти полную реализацию Android и грузится довольно долго.

### Что делать
Если в тесте вообще нет андроидной специфики, перенести тест из `androidTest` в `test` и запускать на хосте.

Если коду требуется что-то из андроида, попробовать использовать `Robolectric`. Это почти полная реализация андроида на хосте. Хотя у этих тестов есть свои недостатки, см. [unnecessary_robolectric](../unnecessary_robolectric).
