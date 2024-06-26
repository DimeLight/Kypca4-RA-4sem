> Увлекательные мучения на ассемблере

# Задача

Составить программу табулирования заданной функции в заданном интервале с заданным шагом:

Используя парадигму структурного программирования в терминах языка ассемблера FASM с функцией записи в файл.

Опять эта функция >:(

y(x)=√(x/(4 ln⁡x ))

вычислил Область Допустимых Значений функции (т.к. тестировщика в проекте нет - будет работать математика):

ОДЗ функции обусловлена присутствием аргумента функции x:

под знаком корня

√x  ⇒ x ≥ 0

под знаком корня в знаменателе дроби в функции натурального логарифма

√( 1 / ln⁡x )  ⇒ 1 / ln⁡x ≥ 0 ⇒ ln⁡x > 0 ⇒ x > 1

Поскольку подкоренное выражение не может быть отрицательно, то значение знаменателя подкоренного выражения строго положительно ( f(x) > 0 ). Значение знаменателя подкоренного выражения f(x) = ln⁡x = 0 при x = 1, следовательно x > 1:

В совокупности:
{x∈R:x>1}

Область Определения Функции:

Стационарные точки:

y(x)<sup>I</sup> = ( √( x / ln⁡x ) / 2 )<sup>I</sup> = 1 / 2 ∙ ( √( x / ln⁡x ) )<sup>I</sup> = 1 / ( 4 √( x / ln⁡x ) ) ( x / ln⁡x )<sup>I</sup> = 1 / ( 4 √( x / ln⁡x ) ) ∙ ( x<sup>I</sup> ∙ ln⁡x -(ln⁡x)<sup>I</sup> ∙ x ) / ln⁡x = ( ln⁡x - 1 ) / ( 4 √( x / ln⁡x ) ln^(2⁡x) ) = 0

x = e – точка минимума.

Минимальное значение функция принимает в:

y(e) = √( e / ( 4 ln⁡e ) ) = √e / 2

Следовательно:

{ y ∈ R : y ≥ √e / 2 }

### График функции:

![image](https://github.com/DimeLight/Kypca4-cpp-3sem/assets/99740101/800c81fa-2e44-4842-a643-169ebf95608c)

Рисунок 1 – график функции

# Детали реализации
## Сообщения
### В поставленной задаче существуют вводные данные, которые не должны существовать (Н: «1/2/3/4», «АБВгдеёж»). Следовательно программа должна уведомить об этом пользователя.

Пример работы

![image](https://github.com/DimeLight/Kypca4-RA-4sem/assets/99740101/125a0a7d-c63a-452e-9971-f999d9c58a7b)

Рисунок 2 – Скриншот консоли программы

![image](https://github.com/DimeLight/Kypca4-RA-4sem/assets/99740101/72e6ceeb-90dc-4971-b7c9-f0f8912c3c5c)

Рисунок 3 – Скриншот работы программы

ЗАКЛЮЧЕНИЕ

В курсовой работе были рассмотрены табулирование и исследование функции.

В ходе выполнения были решены все поставленные задачи.

Проведено математическое исследование функции, в ходе которого была найдена область допустимых значений функции и произведены исключения в вводных данных, что позволило исключить ошибки при табулировании и правильно вывести график. Используя методы структурного программирования, написана программа для табулирования функции. Составлена блок-схема, которая схематично описывает алгоритм решения задачи.

В процессе выполнения курсовой работы усовершенствованы навыки программирования на языке ассемблера FASM 1.73.30.

# СПИСОК ИСПОЛЬЗОВАННЫХ ИСТОЧНИКОВ (откуда пылесосил код и всякое)
+ Рудольф, М. Ассемблер на примерах. Базовый курс.  / М. Рудольф. — Санкт-Петербург: Наука и Техника, 2005. — 240 c. — Текст: непосредственный.
+ ГОСТ 7.32-2017 СИБИД. — Текст : электронный // Техэксперт : [сайт]. — URL: https://docs.cntd.ru/document/1200157208 (дата обращения: 06.12.2021).
+ Генератор библиографического описания. — Текст : электронный // Библиотеки Тольятти : [сайт]. — URL: https://cls.tgl.ru/generator-bo/ (дата обращения: 16.12.2021).
