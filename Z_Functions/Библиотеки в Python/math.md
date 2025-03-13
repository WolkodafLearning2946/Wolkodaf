>[!code]+ Подключить математический модуль
>```py
>import math
>```

> [!abstract]+ import math...
> `math.pi` - число "пи"
> `math.sqrt(x)` - квадратный корень
> `math.sin(x)` - синус угла, заданного ***в радианах***
> `math.cos(x)` - косинус угла, заданного ***в радианах***
> `math.exp(x)` - экспонента $e^x$
> `math.ln(x)` - натуральный логарифм
> `math.floor(x)` - округление "вниз"
> `math.ceil(x)` - округление "вверх"
>>[!example]+ Пример
>>```py
>>import math
>>x = math.floor( 1.6 ) # 1
>>x = math.ceil( 1.6 ) # 2
>>x = math.floor( -1.6 ) # -2
>>x = math.ceil( -1.6 ) # -1

|   |   |
|---|---|
|**Теоретико-числовые функции**|   |
|[`comb(n, k)`](https://docs.python.org/3/library/math.html#math.comb "математика.гребень")|Количество способов выбрать _k_ элементов из _n_ элементов без повторения и без порядка|
|[`factorial(n)`](https://docs.python.org/3/library/math.html#math.factorial "мат.факториал")|_n_ факториал|
|[`gcd(*integers)`](https://docs.python.org/3/library/math.html#math.gcd "математика.нод")|Наибольший общий делитель целых аргументов|
|[`isqrt(n)`](https://docs.python.org/3/library/math.html#math.isqrt "математика.isqrt")|Целый квадратный корень из неотрицательного целого числа _n_|
|[`lcm(*integers)`](https://docs.python.org/3/library/math.html#math.lcm "математика.lcm")|Наименьшее общее кратное целых аргументов|
|[`perm(n, k)`](https://docs.python.org/3/library/math.html#math.perm "математика.perm")|Количество способов выбрать _k_ элементов из _n_ элементов без повторений и с соблюдением порядка|
|**Арифметика с плавающей точкой**|   |
|[`ceil(x)`](https://docs.python.org/3/library/math.html#math.ceil "математика.ceil")|Потолок _x_ , наименьшее целое число, большее или равное _x_|
|[`fabs(x)`](https://docs.python.org/3/library/math.html#math.fabs "математика.fabs")|Абсолютное значение _x_|
|[`floor(x)`](https://docs.python.org/3/library/math.html#math.floor "математика.пол")|Пол _x_ , наибольшее целое число, меньшее или равное _x_|
|[`fma(x, y, z)`](https://docs.python.org/3/library/math.html#math.fma "математика.фма")|Объединенная операция умножения-сложения:`(x * y) + z`|
|[`fmod(x, y)`](https://docs.python.org/3/library/math.html#math.fmod "математика.fmod")|Остаток от деления`x / y`|
|[`modf(x)`](https://docs.python.org/3/library/math.html#math.modf "математика.modf")|Дробные и целые части числа _x_|
|[`remainder(x, y)`](https://docs.python.org/3/library/math.html#math.remainder "math.остаток")|Остаток _x_ относительно _y_|
|[`trunc(x)`](https://docs.python.org/3/library/math.html#math.trunc "математика.trunc")|Целая часть числа _x_|
|**Функции манипулирования числами с плавающей точкой**|   |
|[`copysign(x, y)`](https://docs.python.org/3/library/math.html#math.copysign "математика.копироватьзнак")|Величина (абсолютное значение) _x_ со знаком _y_|
|[`frexp(x)`](https://docs.python.org/3/library/math.html#math.frexp "математика.frexp")|Мантисса и показатель степени _x_|
|[`isclose(a, b, rel_tol, abs_tol)`](https://docs.python.org/3/library/math.html#math.isclose "математика.закрыть")|Проверьте, близки ли значения _a_ и _b_ друг к другу.|
|[`isfinite(x)`](https://docs.python.org/3/library/math.html#math.isfinite "математика.бесконечна")|Проверьте, является ли _x_ ни бесконечностью, ни NaN|
|[`isinf(x)`](https://docs.python.org/3/library/math.html#math.isinf "математика.isinf")|Проверьте, является ли _x_ положительной или отрицательной бесконечностью.|
|[`isnan(x)`](https://docs.python.org/3/library/math.html#math.isnan "математика.иснан")|Проверьте, является ли _x_ NaN (не числом)|
|[`ldexp(x, i)`](https://docs.python.org/3/library/math.html#math.ldexp "математика.ldexp")|`x * (2**i)`, обратная функция[`frexp()`](https://docs.python.org/3/library/math.html#math.frexp "математика.frexp")|
|[`nextafter(x, y, steps)`](https://docs.python.org/3/library/math.html#math.nextafter "математика.следующийпосле")|Значение с плавающей точкой _шаг_ за шагом от _x_ к _y_|
|[`ulp(x)`](https://docs.python.org/3/library/math.html#math.ulp "математика.ulp")|Значение младшего бита _x_|
|**Степенные, показательные и логарифмические функции**|   |
|[`cbrt(x)`](https://docs.python.org/3/library/math.html#math.cbrt "математика.cbrt")|Кубический корень из _x_|
|[`exp(x)`](https://docs.python.org/3/library/math.html#math.exp "математика.exp")|_е,_ возведенное в степень _х_|
|[`exp2(x)`](https://docs.python.org/3/library/math.html#math.exp2 "математика.exp2")|_2_ возведено в степень _x_|
|[`expm1(x)`](https://docs.python.org/3/library/math.html#math.expm1 "математика.expm1")|_e_ возведенное в степень _x_ , минус 1|
|[`log(x, base)`](https://docs.python.org/3/library/math.html#math.log "математика.журнал")|Логарифм _x_ по указанному основанию ( по умолчанию _e_ )|
|[`log1p(x)`](https://docs.python.org/3/library/math.html#math.log1p "математика.log1p")|Натуральный логарифм _1+x_ (основание _e_ )|
|[`log2(x)`](https://docs.python.org/3/library/math.html#math.log2 "математика.log2")|Двоичный логарифм _x_|
|[`log10(x)`](https://docs.python.org/3/library/math.html#math.log10 "математика.log10")|Десятичный логарифм _x_|
|[`pow(x, y)`](https://docs.python.org/3/library/math.html#math.pow "математика.pow")|_x_ возведенный в степень _y_|
|[`sqrt(x)`](https://docs.python.org/3/library/math.html#math.sqrt "математика.sqrt")|Квадратный корень из _x_|
|**Функции суммирования и произведения**|   |
|[`dist(p, q)`](https://docs.python.org/3/library/math.html#math.dist "math.расст")|Евклидово расстояние между двумя точками _p_ и _q_ задано как итерация координат|
|[`fsum(iterable)`](https://docs.python.org/3/library/math.html#math.fsum "математика.fsum")|Сумма значений во входном _итерируемом массиве_|
|[`hypot(*coordinates)`](https://docs.python.org/3/library/math.html#math.hypot "математика.гипотеза")|Евклидова норма итерируемой последовательности координат|
|[`prod(iterable, start)`](https://docs.python.org/3/library/math.html#math.prod "математика.прод")|Произведение элементов входного _итерируемого_ массива с _начальным_ значением|
|[`sumprod(p, q)`](https://docs.python.org/3/library/math.html#math.sumprod "математика.sumprod")|Сумма произведений двух итераций _p_ и _q_|
|**Угловое преобразование**|   |
|[`degrees(x)`](https://docs.python.org/3/library/math.html#math.degrees "математика.степени")|Преобразовать угол _x_ из радиан в градусы|
|[`radians(x)`](https://docs.python.org/3/library/math.html#math.radians "математика.радианы")|Преобразовать угол _x_ из градусов в радианы|
|**Тригонометрические функции**|   |
|[`acos(x)`](https://docs.python.org/3/library/math.html#math.acos "математика.acos")|Арккосинус _x_|
|[`asin(x)`](https://docs.python.org/3/library/math.html#math.asin "математика.asin")|Арксинус _x_|
|[`atan(x)`](https://docs.python.org/3/library/math.html#math.atan "математика.атан")|Арктангенс _x_|
|[`atan2(y, x)`](https://docs.python.org/3/library/math.html#math.atan2 "математика.atan2")|`atan(y / x)`|
|[`cos(x)`](https://docs.python.org/3/library/math.html#math.cos "математика.cos")|Косинус _x_|
|[`sin(x)`](https://docs.python.org/3/library/math.html#math.sin "математика.грех")|Синус _x_|
|[`tan(x)`](https://docs.python.org/3/library/math.html#math.tan "математика.тан")|Тангенс _x_|
|**Гиперболические функции**|   |
|[`acosh(x)`](https://docs.python.org/3/library/math.html#math.acosh "математика.acosh")|Обратный гиперболический косинус _x_|
|[`asinh(x)`](https://docs.python.org/3/library/math.html#math.asinh "математика.asinh")|Обратный гиперболический синус _x_|
|[`atanh(x)`](https://docs.python.org/3/library/math.html#math.atanh "математика.атань")|Обратный гиперболический тангенс _x_|
|[`cosh(x)`](https://docs.python.org/3/library/math.html#math.cosh "математика.cosh")|Гиперболический косинус _x_|
|[`sinh(x)`](https://docs.python.org/3/library/math.html#math.sinh "математика.sinh")|Гиперболический синус _x_|
|[`tanh(x)`](https://docs.python.org/3/library/math.html#math.tanh "математика.tanh")|Гиперболический тангенс _x_|
|**Специальные функции**|   |
|[`erf(x)`](https://docs.python.org/3/library/math.html#math.erf "математика.erf")|[Функция ошибки](https://en.wikipedia.org/wiki/Error_function) в точке _x_|
|[`erfc(x)`](https://docs.python.org/3/library/math.html#math.erfc "математика.erfc")|[Дополнительная функция ошибок](https://en.wikipedia.org/wiki/Error_function) в точке _x_|
|[`gamma(x)`](https://docs.python.org/3/library/math.html#math.gamma "математика.гамма")|[Гамма-функция](https://en.wikipedia.org/wiki/Gamma_function) в точке _x_|
|[`lgamma(x)`](https://docs.python.org/3/library/math.html#math.lgamma "математика.lгамма")|Натуральный логарифм абсолютного значения [гамма-функции](https://en.wikipedia.org/wiki/Gamma_function) в точке _x_|
|**Константы**|   |
|[`pi`](https://docs.python.org/3/library/math.html#math.pi "математика.пи")|_π_ = 3,141592…|
|[`e`](https://docs.python.org/3/library/math.html#math.e "математика.е")|_е_ = 2,718281…|
|[`tau`](https://docs.python.org/3/library/math.html#math.tau "математика.тау")|_τ_ = 2 _π_ = 6,283185…|
|[`inf`](https://docs.python.org/3/library/math.html#math.inf "математика.inf")|Положительная бесконечность|
|[`nan`](https://docs.python.org/3/library/math.html#math.nan "математика.нан")|«Не число» (NaN)|