В Go пакет `strings` предоставляет функции для работы со строками (тип `string`). Он включает в себя инструменты для поиска, замены, разбиения, изменения регистра и других операций над строками.

---
## Основные функции `strings`:
### Поиск и проверка
==Contains(s, substr string)== bool — проверяет, содержит ли строка `s` подстроку `substr`.

> [!code]+
> ```go
> a := "Super puper"  
> fmt.Println(strings.Contains(a, "puper"))
> ```
> > [!output]+
> > ```go
> > true
> > ```

==ContainsAny(s, chars string)== bool — проверяет, содержит ли строка `s` хотя бы один символ из `chars`.

> [!code]+
> ```go
> a := "Super puper"  
> fmt.Println(strings.ContainsAny(a, "xpr"))  
> fmt.Println(strings.ContainsAny(a, "x"))
> ```
> > [!output]+
> > ```go
> > true
> > false
> > ```

==HasPrefix(s, prefix string)== bool — проверяет, начинается ли строка `s` с `prefix`.

> [!code]+
> ```go
> a := "Super puper"  
> fmt.Println(strings.HasPrefix(a, "s"))  
> fmt.Println(strings.HasPrefix(a, "Su"))  
> fmt.Println(strings.HasPrefix(a, "Super puper"))
> ```
> > [!output]+
> > ```go
> > false
> > true
> > true
> > ```

==HasSuffix(s, suffix string)== bool — проверяет, заканчивается ли строка `s` на `suffix`.

> [!code]+
> ```go
> a := "Super puper"  
> fmt.Println(strings.HasSuffix(a, "r"))  
> fmt.Println(strings.HasSuffix(a, " puper"))  
> fmt.Println(strings.HasSuffix(a, "pupe"))
> ```
> > [!output]+
> > ```go
> > true
> > true
> > false
> > ```

==Index(s, substr string)== int — возвращает индекс первого вхождения `substr` в `s`, либо `-1`, если не найдено.

> [!code]+
> ```go
> a := "Super puper"  
> fmt.Println(strings.Index(a, "r"))  
> fmt.Println(strings.Index(a, "per"))  
> fmt.Println(strings.Index(a, " per"))
> ```
> > [!output]+
> > ```go
> > 4
> > 2
> > -1
> > ```

==LastIndex(s, substr string)== int — возвращает индекс последнего вхождения `substr` в `s`.

### Изменение регистра
==ToUpper(s string)== string — переводит строку `s` в **верхний** регистр.
==ToLower(s string)== string — переводит строку `s` в **нижний** регистр.
==Title(s string)== string — делает первую букву каждого слова заглавной.

### Разделение и объединение

### Замена и модификация
==Replace(s, old, new string, n int)== string — заменяет `n` вхождений `old` на `new` в строке `s` (`n < 0` — заменяет все).
==Repeat(s string, count int)== string — повторяет строку `s` `count` раз.
==Trim(s, cutset string) string== — удаляет из `s` все символы, указанные в `cutset`, с обоих концов.
==TrimSpace(s string)== string — удаляет пробелы, табуляции и переносы строк с обоих концов.
==TrimPrefix(s, prefix string)== string — убирает `prefix`, если он есть.
==TrimSuffix(s, suffix string)== string — убирает `suffix`, если он есть.