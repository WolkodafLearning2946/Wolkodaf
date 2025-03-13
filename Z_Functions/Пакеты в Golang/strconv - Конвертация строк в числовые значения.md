Пакет **`strconv`** используется для конвертации строк (`string`) в числовые значения (`int`, `float`, `bool`) и обратно. Он полезен при обработке пользовательского ввода, чтении данных из файлов или работы с API.

---
## Основные функции
### Преобразование строки в число
==Atoi(s string)== (int, error) — преобразует строку в `int`
>[!code]+ Example
>```go
> n, err := strconv.Atoi("42") // n = 42, err = nil
>```

==ParseInt(s string, base int, bitSize int)== (int64, error) - преобразует строку `s` в целое число с указанной системой счисления (`base`: 2, 10, 16 и т. д.).
>[!code]+ Example
>```go
> n, err := strconv.ParseInt("2A", 16, 64) // n = 42, err = nil
>```

==ParseFloat(s string, bitSize int) (float64, error)== - преобразует строку `s` в число с плавающей точкой.
>[!code]+ Example
>```go
> f, err := strconv.ParseFloat("3.14", 64) // f = 3.14, err = nil
>```

### Преобразование числа в строку
==Itoa(i int)== string — преобразует `int` в строку
>[!code]+ Example
>```go
> s := strconv.Itoa(42) // s = "42"
>```

==FormatInt(i int64, base int)== string - преобразует `int64` в строку с указанной системой счисления (`base`: 2, 10, 16 и т. д.)
>[!code]+ Example
>```go
> s := strconv.FormatInt(42, 16) // s = "2a"
>```

==FormatFloat(f float64, fmt byte, prec, bitSize int)== string - преобразует `float64` в строку.

- `fmt`: `'f'` (десятичный), `'e'` (экспоненциальный), `'g'` (оптимальный)

>[!code]+ Example
>```go
> s := strconv.FormatFloat(3.14159, 'f', 2, 64) // s = "3.14"
>```

### Работа с булевыми значениями
==ParseBool(s string)== (bool, error)
**Принимает:** 
- `"1"`, `"t"`, `"T"`, `"true"`, `"TRUE"`, `"True"` → `true`.
- `"0"`, `"f"`, `"F"`, `"false"`, `"FALSE"`, `"False"` → `false`.

>[!code]+ Example
>```go
> b, err := strconv.ParseBool("true") // b = true, err = nil
>```

==FormatBool(b bool)== string
>[!code]+ Example
>```go
> s := strconv.FormatBool(true) // s = "true"
>```