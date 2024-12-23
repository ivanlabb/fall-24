Лабораторная работа 5. Метод опорных векторов.

  В рамках лабораторной работы был реализован метод опорных векторов для задачи бинарной классификации. В рамках алгоритма было реализовано решение двойственной задачи по лямбда для линейного ядра, ядра RBF и полиномиального ядра, для решения задачи была использована функция scipy.optimize.minimize. На основе решения двойственной задачи были высчитаны параметры разделяющей гиперплоскости и построен линейный классификатор.

  Классификатор был протестирован на задаче классификации рака молочной железы (https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset). Данные были подготовлены, после чего был применён разработанный алгоритм. После подбора оптимальных гиперпараметров точности классификаторов оказались следующими:

1) Линейное ядро - 92.4%
2) Ядро RBF - 98.2%
3) Полиномиальное ядро - 94.2%

  Результаты работы алгоритма были сравнены с эталонной реализацией, при аналогичных гиперпараметрах точности оказались следующими:

1) Линейное ядро - 97.7%
2) Ядро RBF - 97.1%
3) Полиномиальное ядро - 97.1%

  Соответственно, на линейном и полиномиальном ядрах точности оказались выше, чем на реализованных вручную алгоритмах, однако самую высокую точность всё равно показал реализованный метод с ядром RBF.

  Результаты работы алгоритма были показаны графически на синтетических данных (поскольку тестовый датасет имел большую размерность). Результаты выглядят следующим образом:

  ![image](https://github.com/user-attachments/assets/1841fbfd-7afc-44a5-93c8-b4fbe26bf2d3)

  ![image](https://github.com/user-attachments/assets/78e7e804-2621-4b83-a63f-b814c4337e8b)

![image](https://github.com/user-attachments/assets/6b4c80c2-9fe0-4e39-9b90-b954a39269ba)


  




