# Цветной вывод

## Библиотека `coloratos` для OneScript для цветного вывода в консоль

> coloratos - игра слов color-text-oscript

----------------------------------------------------

## Шаблон вывода

Вывод формируется по шаблону `(Текст|#color=Цвет)`, где  
- `Текст` - произвольный текст  
- `Цвет` - строковое значение перечисления `ЦветКонсоли.*`

----------------------------------------------------

## Установка

- из локального файла *.ospx: `opm i -f coloratos.ospx`
- с помощью установщика `oscript setup.os VERSION`, где VERSION - номер релиза (см. https://github.com/240596448/coloratos/releases)
- с помощью установщика `oscript setup.os latest` - установка последней версии
- с помощью установщика `oscript setup.os` - интерактивный выбор версии  
> Пример:  
![doc/capture3.png](doc/capture3.png)

----------------------------------------------------


## Примеры использования:

```bsl
#Использовать ".."

ЦветнойВывод.Вывести("Процесс выполнения... ", "Серый");
ЦветнойВывод.ВывестиСтроку("Done", "Зеленый");
``` 
> Результат:  
![doc/capture1.png](doc/capture1.png)

```bsl
#Использовать ".."
ЦветнойВывод.ВывестиСтроку(
		"(Оу!|#color=White) Привет, (Красный!|#color=Красный) Кажется я выгляжу '(малиновым|#color=Малиновый)'.
		|Ты тоже видишь (желтый текст|#color=Желтый) ???", "Синий");
```
> Результат:  
![doc/capture2.png](doc/capture2.png)


***Особенности*** 
- не поддерживаются переносы текста выделяемой подстроки, многоуровневая вложенность шаблона `(Текст|#color=Цвет)`
- не поддерживается установка ЦветаФона
-------------------------------------------------
[-->](test/test.os) Больше примеров в [test/test.os](test/test.os)
