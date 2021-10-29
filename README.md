# Annotation @Qualifier

## Задача

1. При условии, что есть несколько бинов, которые можно внедрить, необходимо  обозначить какой именно бин  хотим внедрить.

## Решение

1. Указываем у бина аннотацию и в скобках id бина, который  хотим внедрить.
2. Когда внедрение производится с помощью конструктора, аннотацию необходимо указывать рядом  с аргументами конструктора.
3. Первый этап - внедрение по полю - меняем `MusicPlayer`.
4. Без аннтоации `@Qualifier` выдается ошибка, так как для внедрения подходит два бина - `classicalMusic` и `rockMusic`.
5. Чтобы решить проблему - пишем аннотацию к полю `music` и указываем id `classicalMusic`.
6. При запуске - `Computer 1 Playing: Classic` - все работает.
7. В следующем репо - внедрение через конструктор.
