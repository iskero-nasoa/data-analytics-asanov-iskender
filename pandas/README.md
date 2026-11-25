Task 1 — Inspect the Dataset
Check the number of rows and columns, data types of all columns, and data types of selected columns such as Salary, Age, and HireDate. Use notna() to identify rows where Salary is present. Identify all data-quality problems: missing values, duplicates, inconsistent department names, incorrect age, and dates stored as text. Remove extra spaces if any. Check whether all values in PerformanceScore are numeric.

Task 2 — Handle Missing Salaries
Find missing values, count them by column, and calculate the percentage of missing values. Replace "unknown" in Salary with a missing value, convert Salary to a numeric type using errors="coerce", and replace empty Salary values with the median salary.
Experiment with dropna() using axis, how, subset, and thresh. Explain what changes with each parameter.
Task 3 — Standardize Department Names
Clean the Department column by removing extra spaces, making the naming consistent, and using str.replace() if needed. Check unique values after cleaning. Find the employee with an incorrect age value and decide how to handle it.

Task 4 — Remove Duplicates
Identify and eliminate duplicate employee records to ensure accurate employee counts. First remove exact duplicates, then remove duplicates by EmployeeID. Experiment with drop_duplicates() using subset, keep="first", keep="last", and keep=False.

Task 5 — Convert Data Types
Convert Age to a nullable integer type and convert Department and Gender to category type. Check the data types after each conversion. Explain the difference between object and category.
Convert PerformanceScore to a numeric type if needed
Task 6 — Parse Hire Dates
Convert text-based dates into a proper datetime format to enable time-based analysis. Extract the year, month, and weekday from HireDate. Calculate the number of years each employee has worked in the company.

Task 7 — Rename Columns and Merge Datasets
Rename Salary to MonthlySalary and HireDate to EmploymentStartDate using rename() with the columns parameter. Combine the employee data with department information using a common key such as Department or DepartmentName. Use how="left" to keep all employees and check whether the merge created missing values.

Task 8 — Final Check and Summary
Check the final data types, missing values, number of rows and columns, duplicates, and date types. Make sure department names are consistent and there are no duplicate employees. Write a short summary explaining what problems you found, which methods and parameters you used, and why data preparation is important before HR analysis.


Задание 1 — Изучение набора данных
Проверьте количество строк и столбцов, типы данных для всех столбцов, а также типы данных для отдельных колонок, таких как `Salary` (зарплата), `Age` (возраст) и `HireDate` (дата найма). Используйте метод `notna()`, чтобы определить строки, в которых указана зарплата (`Salary`). Выявите все проблемы с качеством данных: пропущенные значения, дубликаты, несоответствия в названиях отделов, некорректные значения возраста, а также даты, сохраненные в текстовом формате. Удалите лишние пробелы, если они есть. Проверьте, являются ли все значения в столбце `PerformanceScore` (оценка эффективности) числовыми.

Задание 2 — Обработка пропущенных значений в столбце «Зарплата»
Найдите пропущенные значения, подсчитайте их количество в каждом столбце и вычислите процент пропусков. Замените значение «unknown» (неизвестно) в столбце `Salary` на пропуск (NaN), преобразуйте столбец `Salary` в числовой формат (используя `errors='coerce'`), а затем заполните пустые значения медианной зарплатой.
Поэкспериментируйте с методом `dropna()`, используя параметры `axis`, `how`, `subset` и `thresh`. Объясните, как меняется результат при использовании каждого из этих параметров.

Задание 3 — Стандартизация названий отделов
Приведите столбец `Department` (отдел) в порядок: удалите лишние пробелы, унифицируйте названия (при необходимости воспользуйтесь методом `str.replace()`). После очистки проверьте уникальные значения в этом столбце. Найдите запись о сотруднике с некорректным возрастом и решите, как поступить с этой ошибкой.

Задание 4 — Удаление дубликатов
Выявите и удалите дублирующиеся записи о сотрудниках, чтобы обеспечить точность их подсчета. Сначала удалите полные дубликаты строк, а затем — дубликаты, основываясь на идентификаторе сотрудника (`EmployeeID`). Поэкспериментируйте с методом `drop_duplicates()`, используя параметры `subset`, а также аргументы `keep='first'`, `keep='last'` и `keep=False`.

Задание 5 — Преобразование типов данных
Преобразуйте столбец `Age` в целочисленный тип, допускающий пропуски (nullable integer), а столбцы `Department` и `Gender` (пол) — в категориальный тип (`category`). Проверяйте типы данных после каждого преобразования. Объясните, в чем заключается различие между типами `object` и `category`. При необходимости преобразуйте столбец `PerformanceScore` в числовой тип.

Задача 6 — Обработка дат найма
Преобразуйте даты, представленные в текстовом формате, в надлежащий формат даты и времени (datetime), чтобы обеспечить возможность анализа временных показателей. Извлеките из столбца `HireDate` год, месяц и день недели. Рассчитайте, сколько лет каждый сотрудник проработал в компании.

Задача 7 — Переименование столбцов и объединение наборов данных
Переименуйте столбец `Salary` в `MonthlySalary`, а `HireDate` — в `EmploymentStartDate`, используя метод `rename()` с параметром `columns`. Объедините данные о сотрудниках с информацией о подразделениях, используя общий ключ (например, `Department` или `DepartmentName`). Примените параметр `how="left"`, чтобы сохранить в итоговом наборе всех сотрудников, и проверьте, не появились ли в результате объединения пропущенные значения.

Задача 8 — Итоговая проверка и выводы
Проверьте финальные типы данных, наличие пропущенных значений, количество строк и столбцов, наличие дубликатов, а также корректность форматов дат. Убедитесь, что названия подразделений единообразны и в данных отсутствуют дублирующиеся записи о сотрудниках. Составьте краткое резюме: опишите выявленные проблемы, укажите использованные методы и параметры, а также объясните, почему подготовка данных важна перед проведением HR-анализа.