 Работа с госзатратами.
 
Я решила собрать данные из госкаталога. Для этого я решила взять 2 параметра: минимальная сумма контракта в рублях (100.000.000) и максимальная сумма контракта в рублях (20.000.000.000), потому что иначе датасет был слишком маленьким. При этом для усложнения кода я также решила поставить ограничения в виде дат - границы составления контрактов. Для удобства я использовала библиотеку datetime, так как без дополнительных настроек не получалось парсить достаточное количество строк.
    
Чтобы реализовать возможность сбора больше, чем 500 строк, я решила воспользоваться библиотекой time, чтобы иметь возможность, когда возникнет ошибка вследствие превышения количества парсинга возможных строк, поставить код "на паузу".

 
 Результаты и выводы:
    У меня получилось собрать 1520 записей из Госзакупок, бюджет которых был от 100.000.000 до 20.000.000.000 рублей, в период с 2005 до 2023 года включительно. Благодаря срезам данных и визуализации я заметила, что: 1. Государственные контракты распределены неравномерно между регионами. Крупные экономические центры, такие как Москва и Санкт-Петербург получают значительные объемы финансирования, отчего могут страдать более мелкие регионы. 2. В некоторых регионах преобладают мелкие заказы (большое количество контрактов с небольшой суммой), в то время как в других — крупные проекты (меньше контрактов, но с большими суммами).3. Некоторые регионы, такие как Ямало-Ненецкий автономный округ, выделяются высокой средней и максимальной суммой контрактов, что может быть связано с крупными инфраструктурными или промышленными проектами.
