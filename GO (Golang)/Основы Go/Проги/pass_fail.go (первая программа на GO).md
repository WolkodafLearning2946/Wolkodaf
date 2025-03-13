>[!code]+
>```go
> // pass_fail сообщает, сдал ли пользователь экзамен.  
> package main  
>   
> import (  
>     "bufio"  
>     "fmt"    
>     "log"    
>     "os"    
>     "strconv"   
>      "strings")  
>   
> func main() {  
>     fmt.Print("Enter a grade: ")          // запрашивает у пользователя значение  
>     reader := bufio.NewReader(os.Stdin)   // создаём bufio.Reader для чтения ввода с клавиатуры  
>     input, err := reader.ReadString('\n') // читаем данные, вводимые пользователем до нажатия клавиши Enter  
>     if err != nil {  
>        log.Fatal(err) // если произошла ошибка, вывести сообщение и прервать работу программы  
>     }  
>     input = strings.TrimSpace(input)            // удаляем символ новой строки из введённых данных  
>     grade, err := strconv.ParseFloat(input, 64) // преобразовать строку в значение float64 (число)  
>     if err != nil {  
>        log.Fatal(err)  
>     }  
>     status := "" // объявление переменной в нужной области видимости для выведения ответа (в границах функции)  
>     if grade >= 60 {  
>        status = "passing"  
>     } else {  
>        status = "failing"  
>     }  
>     fmt.Println("A grade of", grade, "is", status)  
> }
>```