# global_lab_python
architecture of computer laboratory work

Цель: калькулятор с интерактивной оболочкой, переводящий числа с введенной пользователем системы счисления в другую.
Программа разбита по версиям, указанных в каждом имени как lab_0_n.py, где n - номер лабораторной работы. 
stud_lib.py - библиотека содержащая в себе такие функции:

**checkalph(A,X)** - проверяет вхождения массива *A* в массив *X*. Возвращает "True"/"False"

**create_array(integer_array,float_array,text)** - превращает введенный текст в массивы *integer_array*, где хранятся целые числа вида 0-F, *float_array*, где хранится всё после точки, *text* - строка, которую нужно переконвертировать (текст задаётся в виде 123.456 как число с плавающей точкой, либо 123 как целое число);

**convert(var_input,var_output,text)** - конвертирует с системы *var_input* в систему *var_output* переменную *text*. возвращает результат.

**init_code(k)** - представляет целое число *k* в диапазоне [-128;127] в прямом, обратном и дополнительном двоичном коде. Возвращает соответственные переменные.

**convert_neg_code(neg_code)** - конвертирует переменную *neg_code* в целочисленный вид. Принимает первое число за знак (1 - минус, 0 - плюс). Возвращает десятичное представление, переработанное методом **convert**

**sum_neg_code(neg_code_one,neg_code_two,count_rank)** - суммирует два двоичных числа *neg_code_one* и *neg_code_two* в обратном коде. Принимает значение *count_rank* (степень числа 2) для ограничения разрядности. Используется метод **convert_neg_code** для проверки на перезаполнение разрядной сетки. Если число входит в рязрядную сетку, возвращает результат в десятичном виде. Иначе возвращает уведомление об ошибке.

Первая загруженная версия lab_0_5:
  - добавлена возможность конвертировать числа с плавающей точкой. В список алфавита добавлен элемент '.'
  - добавлен счётчик dots_count, который проверяет количество точек в введённой пользователем переменной text (если > 1, то прерывает выполнение)

20.march.2017     23:55

Версия lab_0_6:
  - В lab_01_test.py (main prog) добавлен вариант выбора между интегрированными программами (1 - конвертация между системами счисления, 2 - представление двоичного кода в разных вариациях)
  - В stub_lib.py добавлена функция init_code, которая позволяет переработать целочисленный тип данных в диапазоне от [-128;127] и представить его в двоичном коде: прямой код, обратный код, дополнительный код. Соответственно возвращает 3 переменных.

Версия lab_0_7:
  - В lab_01_test.py (main prog) добавлен вариант выбора прибавления/отнимания двоичных чисел в обратном представлении.
  - В stub_lib.py добавлена функция convert_neg_code, которая конвертирует число из обратного двоичного в десятичный код. При этом учитывается первый символ строки, которую считывает функция, где "1" принимается за знак минуса, "0" за знак плюса. Возвращает полученный результат в десятичном представлении.
  - В stud_lib.py добавлена функция sum_neg_code, которая проводит операцию сложения (вычитания) двоичных чисел в обратном представлении. Возвращает полученный результат в десятичном представлении.
  - Фикс функции convert (раньше возвращала результат двоичного числа в интервале [0;9] с лишним нулём) методом round на возврате результата.
  - Убраны лишние комментарии.


19.april.2017     10:19
