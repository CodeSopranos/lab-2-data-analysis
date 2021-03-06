#  Методы снижения размерности (PCA, MDS)

**Задача.** В Excel таблице собраны персональные данные клиентов банка. Столбцы таблицы
отражают следующие сведения о клиенте

| 1 | 2 | 3 | 4 | 5 | 6 |
| - | - | - | - | - | -|
| Возраст (лет)  | Количество иждивенцев     | Доход (руб./мес.)| Срок проживания в регионе (лет) | Оценка автомобиля заемщика (USD) | Размер кредита (тыс. руб.)|

### Данные.

Выполнить первичную обработку данных. Сделать первые выводы.

### Снижение размерности с помощью PCA
- Выполнить центрирование данных и такую нормировку, что евклидова норма каждого признака
равна 1 (полученная матрица обозначается через Z).
- Найти SVD разложение матрицы Z (матрицы U, S, V). Докажите, что при выбранной
нормировке, коэффициенты разложения столбцов матрицы Z по скрытым факторам являются
корреляциями этих столбцов и скрытых факторов.
- Исследуйте, сколько скрытых факторов (главные факторы) достаточно для хорошей
аппроксимации матрицы данных Z. Заменить значения исходных признаков линейными
комбинациями главных факторов (матрица Z k , k – число главных факторов). Оценить
погрешность аппроксимации в евклидовой матричной норме и норме Фробениуса.
- Сравнить матрицы корреляций признаков для матрицы Z и матрицы Z k . Оценить качество
аппроксимации по близости матриц корреляций (можно использовать относительную
погрешность в одной из матричных норм)
- Используя выделенные главные факторы, найти представления клиентов векторами меньшей
размерности (размерности k).
- Используя представление клиентов векторами меньшей размерности, построить карту
клиентов. Сделать выводы о клиентах банка.

### Интерпретация скрытых факторов.
- Выписать матрицу коэффициентов разложения признаков z j по главным факторам. Исследовать
структуру этой матрицы с целью выделения групп признаков тесно связанных с каждым из
главных факторов.
- На основе анализа структуры матрицы коэффициентов разложения, предложить интерпретацию
выделенным главным факторам.
- Дать интерпретацию построенной выше карте клиентов.
- Выполнить вращения в пространстве главных факторов с целью улучшения структуры матрицы
коэффициентов разложения признаков z j по главным факторам. В случае улучшения структуры,
найти новое представление клиентов векторами меньшей размерности (размерности k).
Построить улучшенную карту клиентов и дать ее интерпретацию.

### Снижение размерности с помощью MDS
- Предложите способ вычисления расстояния между клиентами и вычислите матрицу
расстояний.
- Проверьте, можно ли клиентов банка поместить в евклидово пространство размерности 2 с
сохранением расстояний между клиентами.
- используйте любой из алгоритмов MDS для размещения объектов в евклидовом пространстве
размерности 2. Оцените погрешность такого размещения. Постройте карту клиентов.
- Сравните с картами клиентов из предыдущих пунктов и сделайте выводы.
