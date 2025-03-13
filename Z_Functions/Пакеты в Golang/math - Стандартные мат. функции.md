Пакет **`math`** предоставляет стандартные математические функции для работы с числами с плавающей точкой (`float32`, `float64`). Он не поддерживает `int`, но можно использовать приведение типов.

---
## Основные функции пакета `math`
### Константы
- **`math.Pi`** = 3.141592653589793
- **`math.E`** = 2.718281828459045
- **`math.Phi`** = 1.618033988749895 (золотое сечение)
- **`math.Sqrt2`** = 1.4142135623730951 (корень из 2)

### Арифметические операции
- **`math.Abs(x float64) float64`** — модуль числа.
- **`math.Ceil(x float64) float64`** — округление вверх.
- **`math.Floor(x float64) float64`** — округление вниз.
- **`math.Round(x float64) float64`** — округление до ближайшего целого.
- **`math.Trunc(x float64) float64`** — отбрасывание дробной части.
- **`math.Mod(x, y float64) float64`** — остаток от деления.
- **`math.Pow(x, y float64) float64`** — возведение `x` в степень `y`.
- **`math.Sqrt(x float64) float64`** — квадратный корень.
- **`math.Cbrt(x float64) float64`** — кубический корень.

>[!code]+ Example
>```go
> package main
> 
> import (
> 	"fmt"
> 	"math"
> )
> 
> func main() {
> 	fmt.Println(math.Abs(-7.5))  // 7.5
> 	fmt.Println(math.Ceil(3.2))  // 4
> 	fmt.Println(math.Floor(3.8)) // 3
> 	fmt.Println(math.Round(2.5)) // 3
> 	fmt.Println(math.Mod(10, 3)) // 1
> 	fmt.Println(math.Sqrt(16))   // 4
> 	fmt.Println(math.Pow(2, 3))  // 8
> }
>```

### Тригонометрия

- **`math.Sin(x float64) float64`** — синус.
- **`math.Cos(x float64) float64`** — косинус.
- **`math.Tan(x float64) float64`** — тангенс.
- **`math.Asin(x float64) float64`** — арксинус.
- **`math.Acos(x float64) float64`** — арккосинус.
- **`math.Atan(x float64) float64`** — арктангенс.
- **`math.Atan2(y, x float64) float64`** — арктангенс с учетом квадранта.

>[!code]+ Example
>```go
> fmt.Println(math.Sin(math.Pi / 2)) // 1
> fmt.Println(math.Cos(0))           // 1
> fmt.Println(math.Tan(math.Pi / 4)) // 1
>```

### Логарифмы и экспоненты
- **`math.Exp(x float64) float64`** — e^x.
- **`math.Log(x float64) float64`** — натуральный логарифм (по основанию e).
- **`math.Log10(x float64) float64`** — десятичный логарифм.
- **`math.Log2(x float64) float64`** — двоичный логарифм.

>[!code]+ Example
>```go
> fmt.Println(math.Exp(1))      // 2.718281828459045 (math.E)
> fmt.Println(math.Log(math.E)) // 1
> fmt.Println(math.Log10(100))  // 2
> fmt.Println(math.Log2(8))     // 3
>```

## Основные функции `math/rand`
### Генерация случайных чисел
- **`rand.Intn(n int) int`** — случайное число от `0` до `n-1`
- **`rand.Float64() float64`** — случайное число в диапазоне `[0.0, 1.0)`.
- **`rand.Float32() float32`** — случайное число в диапазоне `[0.0, 1.0)`.
- **`rand.Int() int`** — случайное число типа `int`.

### Установка "зерна" (seed)
По умолчанию `rand` **генерирует одинаковую последовательность чисел** при каждом запуске.  
Чтобы сделать числа **разными при каждом запуске**, нужно задать случайное зерно (`seed`).

- **`rand.Seed(n int64)`** — задаёт начальное значение генератора.  

<u>**Обычно используют текущее время:**</u>
>[!code]+
>```go
> package main
> 
> import (
> 	"fmt"
> 	"math/rand"
> 	"time"
> )
> 
> func main() {
> 	rand.Seed(time.Now().UnixNano()) // Уникальное seed на основе времени
> 	fmt.Println(rand.Intn(100))      // Всегда разное число от 0 до 99
> }
>```