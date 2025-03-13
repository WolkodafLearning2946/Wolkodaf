>[!code]+
>```go
> package main  
>   
> import (  
>     "errors"  
>     "fmt")  
>   
> func main() {  
>     err := errors.New("height can't be negative") // Создаём новое значение ошибки  
>     fmt.Println(err.Error()) // Возвращает сообщение об ошибке  
> }
>```

---
head first страница 130