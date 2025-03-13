
---
## Свои исследования

> [!info]+ ==os.Args== - это срез аргументов командной строки, переданных программе при запуске
> - `os.Args[0]` — это имя исполняемого файла (стандарт)
> - `os.Args[1]`, `os.Args[2]`, ... — это переданные аргументы

> [!code]+
> ```go
> package main  
>   
> import (  
>     "fmt"  
>     "os")  
>   
> func main() {  
>     fmt.Println("Полный список аргументов:", os.Args[1:])  
>   
>     if len(os.Args) > 1 {  
>        fmt.Println("Первый аргумент:", os.Args[1])  
>     } else {  
>        fmt.Println("Аргументы не переданы.")  
>     }  
> }
> ```
>
> >[!terminal]+
> >```sh
> > go run main.go Hello World
> >```
> 
> > [!output]+
> > ```
> > Полный список аргументов: [Hello World]
> > Первый аргумент: Hello
> > ```



