# BOA* и другие алгоритмы двукритериального поиска.

В данном проекте мы изучали алгоритмы двукритериального поиска в графе. Это алгоритмы, в которых у путей есть две характеристики (к примеру, расстояние и время), и путь называется оптимальным, если нет другого пути, который лучше данного по обеим характеристикам. Более подробно про проект можно прочитать в нашем pdf-тексте.

Все алгоритмы находятся в папке `algo`. Там есть 6 алгоритмов:

* `BruteForce`
* `Bdijkstra`
* `BBdijkstra`
* `NAMOA_star`
* `NAMOA_star_dr`
* `BOAStar`

Алгоритм `BruteForce` перебирает все пути в графе и предназначен для проверки алгоритма `BDijkstra` на правильность на маленьких тестах. Для запуска на реальных тестах он не пригоден.

Остальные алгортимы можно запускать на тестах, находящихся в папке `maps`. Достаточно запустить алгоритм при помощи скрипта `run.sh` и будут запущены все тесты со разными вариантами эвристик. Пример запуска:

```
./run.sh BOAStar
```

Промежуточные результаты работы будут выводиться в консоль, а после завершения работы окончательные результаты можно будет найти в выходных файлах.

* Файл `results_<algorithm name>_cal.txt` содержит статистику по каждой карте и эвристике для алгоритма: среднее время работы, медиана и т.д. А также средний размер множества Парето (должны совпадать для разных алгоритмов, разумеется).
* Также в папке `results/<map name>/`  в файле `<algorithm name>.txt` будут находиться ответы на все тесты.
* Кроме того в той же папке в файле `<algorithm name>_runtimes.txt` можно найти время работы каждого теста.


Файл `algo/results/Results.ipynb` содержит построение графиков и таблиц для сравнения алгоритмов по времени работы.
