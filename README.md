# Door-and-chair-problem
Задача компьютерного зрения: определение возможности перенести объект через дверной проём

## Постановка задачи

Пользователь на вход алгоритма даёт фотографию, на которой есть только стул и дверной проём.

Алгоритм должен уметь определять по фотографии, можно ли стул поступательным движением пронести через дверной проём (т.е дать ответ "да" / "нет").

Опциональная задача для алгоритма: указать, на сколько градусов надо повернуть стул, чтобы он стал пролезать через дверной проем.

## Требования к входным данным
 
Входные изображения пользователя должны соответствовать следующим требованиям:
 
- Формат jpg
- На фотографиях есть только стул и дверной проём. Наличие других предметов крайне нежелательно.
- Стул и дверь должны целиком влезать в кадр
- Фотографии должны быть сделаны при хорошем освещении
- Наличие большого числа теней нежелательно

## Описание алгоритма

1. Детектирование стула с помощью ORB-детектора. При этом применяется подбор "наилучшего" шаблона для стула
2. По данным п.1 определение ширины фигуры стула 
3. Детектирование двери с помощью преобразования Хафа для прямых
4. По данным п.3 определение ширины проёма
5. Сравнение ширины стула и проёма, выдача вердикта "да"/"нет"

## Реализация
(в файле project.ipynb)

## Отчёт

(в файле project.ipynb)
