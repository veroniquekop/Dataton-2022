Аннотация проекта

Суть проекта - реализовать ассистент терапевта, который в онлайн формате на основании рубрикатора клинических рекомендаций формирует предварительный диагноз.

В реализации нашего проекта “Ассистент терапевта” лежит датасет наиболее часто встречающихся заболеваний в практике врача-терапевта. 

Данный датасет собран на основе рубрикатора клинических рекомендаций и включает в себя клинико-диагностические признаки о заболеваниях.

Датасет представляет собой следующую структуру https://docs.google.com/spreadsheets/d/14Pb2RGetY-Cl6R7MrvchFYOcddj7uSrWIwlyCMFTjZk/edit#gid=0:

- [ ] Диагноз	
- [ ] Жалобы	
- [ ] Анамнез заболеваний	
- [ ] Анамнез жизни	
- [ ] Данные объективного осмотра	
- [ ] Лабораторные методы исследования	
- [ ] Инструментальные методы исследования	
- [ ] Рекомендации _(заполняется действующей группой врачей соответствующей специализации)_					

На основании данных, вводимым врачом (по результатам первичного осмотра) выводится наиболее вероятный диагноз и первоначальные рекомендации для пациента.

_Описание предварительных результатов:_ введенный симптом(-ы) в процентном соотношении отображает предварительный диагноз(-ы) и рекомендации от терапевта.
__________________________________________________________________

Нами была создана ML-модель, которая по введенному признаку(-ам) предсказывает с определенной вероятностью тот или иной диагноз: https://colab.research.google.com/drive/1vbbhIVqYshl74TwtnNetRfzJzoc3Ud3I#scrollTo=ngvSsPyrqm_V

Менять значение можно в строке *query_str*.

Модель использует файл therapy.csv, который в настоящее время продолжает заполняться данными.

Используемые источники для датасета:

1. Рубрикатора клинических рекомендаций https://cr.minzdrav.gov.ru/rubricator 
2. Сайт для практикующих доктров https://medi.ru/
