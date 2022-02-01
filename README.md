# Ноутбук Discret_optimize_Deikstra.ipynb

содержит:

### Алгоритм Дейкстры

- Алгоритм позволяет за время O(n^2) находить кратчайший путь из заданной вершины во все остальные вершины графа.
- Алгоритм позволяет также найти все связанные компоненты. Для этого нужно взять произвольную вершину графа в качстве стартовой. Запустить алгоритм и посмотреть на множество вершин в массиве fishka, где храняться вершины найденной компоненты. Далее нужно пересечь вершины графа с множеством fishka и выбрать в оставшемся множестве стартовую вершину. И т.д. пока не останется вершин в графе, не побывавших в массиве fishka.
- Алгоритм позволяет выбросить из графа тяжелые ребра и получить его остовное дерево закодированнное в v_dist.

### Применение алгоритма в дискретной оптимизации. Пример динамического программирования

Компания хочет выполнить дополнительную работу в течение 5 месяцев. Она решила, что для выполнения задачи ей нужно иметь в 1й месяц 10 сотрудников, во 2й - 7, в 3й - 9, в 4й - 8 и в 5й - 11. 
При этом она несет затраты:
- на обучение 800 евро/ч
- на увольнение 1200 евро/ч
- на лишнего сотрудника 1600 евро/мес.

Теперь ей нужно решить какое дополнительное количество сотрудников нанять, чтобы общие затраты были минимальные.

Понятно, что в любой месяц в компании должно быть не менее $b_i$ и не более 11 сотрудников.

~~ Разбор решения приводится в ноутбуке. ~~
![Граф](https://github.com/SZGraph/discrete_optimization-/blob/76300f28a7edd8f9ba61aa6e1951da462469e5a1/%D0%94%D0%B8%D1%81%D0%BA%D1%80%D0%B5%D1%82%D0%BD%D0%B0%D1%8F%20%D0%BE%D0%BF%D1%82%D0%B8%D0%BC%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F.png "Решение задачи")

**Задача решается нахождением минимального маршрута в графе G(V,E) между вершинами (0,0) и (6,0) с помощью `алгоритма Дейкстры`.**

[Пример взят из Alexander Schrijver. A Course in Combinatorial Optimization. 2017. 221 p.]
