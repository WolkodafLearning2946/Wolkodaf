>[!code]+
>```go
> // guess - игра, в которой игрок должен угадать случаное число  
> package main  
>   
> import (  
>     "bufio"  
>     "fmt"    
>     "log"    
>     "math/rand" // `путь импортирования пакета`. Intn - имя пакета  
>     "os"  
>     "strconv"    
>     "strings"    
>     "time" // импорт пакета "time"  
> )  
>   
> func main() {  
>     seconds := time.Now().Unix() // получаем текущую дату и время в формате целого числа  
>     // Unix — целое количество секунд, прошедших с 1 января 1970 года    
>     rand.Seed(seconds)           // функция генератора случайных чисел. Теперь генерируемые числа будут разными при каждом запуске. УСТАРЕЛО!  
>     target := rand.Intn(100) + 1 // генерация случайного числа от 0 до 99. + 1  
>     fmt.Println("I've chosen a random number between 1 and 100.")  
>     fmt.Println("Can you guess it?")  
>   
>     reader := bufio.NewReader(os.Stdin) // создаём bufio.Reader для чтения ввода с клавиатуры  
>   
>     success := false  
>     for guesses := 0; guesses < 10; guesses++ {  
>        fmt.Println("You have", 10-guesses, "guesses left.")  
>   
>        fmt.Print("Make a guess: ")           // запросить число  
>        input, err := reader.ReadString('\n') // прочитать данные, введённые пользователем до нажатия Enter  
>        if err != nil {  
>           log.Fatal(err) // из-за возврата двух значений  
>        }  
>        input = strings.TrimSpace(input)  // удаление символа новой строки  
>        guess, err := strconv.Atoi(input) // входная строка преобразуется в целое число  
>        if err != nil {  
>           log.Fatal(err)  
>        }  
>        if guess < target {  
>           fmt.Println("Oops. Your guess was LOW") // если предположение игрока МЕНЬШЕ загаданного числа  
>        } else if guess > target {  
>           fmt.Println("Oops. Your guess was HIGH") // если предположение игрока БОЛЬШЕ загаданного числа  
>        } else if guess == target {  
>           fmt.Println("Good job! You guesses it!")  
>           success = true  
>           break  
>        }  
>     }  
>     if !success {  
>        fmt.Println("Sorry. You didn't guess my number. It was:", target)  
>     }  
> }
>```