Лабораторная работа №6. Регрессия
Выполнил: Лабуткин Иван Алексеевич

В рамках лабораторной работы был создан класс RidgeRegressor, решающий задачу гребневой регрессии через сингулярное разложение. Он был реализован в двух вариациях: без свободного члена и без него. В классе были реализованы методы fit (обучение), fit_just_weight (обучение, но без сингулярного разложение, нужно для пересчёта весов при другом параметре регуляризации), predict, count_Q (расчёт функционала потерь), choose_t (построение графика зависимости функционала потерь от значения параметра регуляризации) и cond_number (расчёт числа обусловленности матрицы).
Без задания параметра регуляризации (т.е. при решении задачи линейной регрессии) R^2 на тестовой выборке у регрессора без свободного члена был равен 0.694, со свободным членом - 0.989. Далее был проведён оптимальный подбор параметра регуляризации на валидационной выборке, в результате чего были построены графики зависимости функции потерь от значения параметра регуляризации.
Для регрессора без свободного члена график выглядел следующим образом:

![image](https://github.com/user-attachments/assets/3ae1488d-958d-4881-9ce6-23b82e833edf)

Для регрессора со свободным членом график был следующий:

![image](https://github.com/user-attachments/assets/7da2a949-ae05-4f06-afeb-66614db6cca6)

Оптимальное значение параметра в первом случае оказалось равным 235000. При таком значении R^2 регрессора на тестовой выборке повысился до 0.808.
Во втором случае регрессия не нуждалась в регуляризации, поэтому параметр остался быть равным 0.

Для сравнения с эталонной реализацией был выбран наиболее точный метод (без регуляризации со свободным членом) из реализованных вручную и метод из sklearn с точно такими же гиперпараметрами. Результаты оказались идентичными

