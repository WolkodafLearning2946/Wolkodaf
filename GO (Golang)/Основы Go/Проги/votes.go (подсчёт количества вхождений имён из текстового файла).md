>[!code]+ `votes.txt` - Текстовый файл
>```
> Amber Graham
> Brian Martin
> Amber Graham
> Brian Martin
> Amber Graham
>```

>[!code]+ `datafile.go` - Пакет
>```go
> // Пакет datafile предназначен для чтения данных из файла  
> package datafile  
>   
> import (  
>     "bufio"  
>     "os")  
>   
> func GetStrings(fileName string) ([]string, error) {  
>     var lines []string  
>     file, err := os.Open(fileName)  
>     if err != nil {  
>        return nil, err  
>     }  
>     scanner := bufio.NewScanner(file)  
>   
>     for scanner.Scan() {  
>        line := scanner.Text()  
>        lines = append(lines, line)  
>     }  
>   
>     err = file.Close()  
>   
>     if err != nil {  
>        return nil, err  
>     }  
>     if scanner.Err() != nil {  
>        return nil, scanner.Err()  
>     }  
>     return lines, nil  
> }
>```

> [!code]+ `votes.go` - Способ 1
> ```go
> // votes.go - подсчитывает имена в файле. С помощью сегментов  
> package main  
>   
> import (  
>     "GoTest/datafile"  
>     "fmt"    
>     "log"
> )  
>   
> func main() {  
>     lines, err := datafile.GetStrings("votes.txt")  
>     if err != nil {  
>        log.Fatal(err)  
>     }  
>     var names []string  
>     var counts []int  
>     for _, line := range lines {  
>        matched := false  
>        for i, name := range names {  
>           if name == line {  
>              counts[i]++  
>              matched = true  
>           }  
>        }  
>        if matched == false {  
>           names = append(names, line)  
>           counts = append(counts, 1)  
>        }  
>     }  
>     for i, name := range names {  
>        fmt.Printf("%s: %d\n", name, counts[i])  
>     }  
> }
> ```
> > [!output]+
> > ```
> > Amber Graham: 3
> > Brian Martin: 2
> > ```

> [!code]+ `votes1.go` - Способ 2
> ```go
> // votes1.go - подсчитывает имена в файле. С помощью карт  
> package main  
>   
> import (  
>     "GoTest/datafile"  
>     "fmt"    "log")  
>   
> func main() {  
>     lines, err := datafile.GetStrings("votes.txt")  
>     if err != nil {  
>        log.Fatal(err)  
>     }  
>   
>     counts := map[string]int{}  
>     for _, line := range lines {  
>        counts[line]++ // Увеличивает счётчик голосов для текущего кандидата  
>     }  
>   
>     for name, count := range counts {  
>        fmt.Printf("Votes for %s: %d\n", name, count)  
>     }  
> }
> ```
> > [!output]+
> > ```
> > Votes for Amber Graham: 3
> > Votes for Brian Martin: 2
> > ```



