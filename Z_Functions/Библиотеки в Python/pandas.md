> [!info]+ Импорт библиотеки
> ```py
> import pandas as pd
> # pd - псевдоним ( может быть любой ) 
> ```

> [!code]+
> ```py
> import pandas as pd  
>   
> bank_db = {  
>     'Name' : ['Ivan Ivanovich', 'Ivan Petrovich'],  
>     'Age' : [0,1],  
>     'Experience' : [4,7],  
>     'Salary' : [75,95],  
>     'Credit_score' : [4,8],  
>     'Outcome' : [0,1]  
> }  
>   
> df = pd.DataFrame(bank_db)  
> print(df) # Таблица данных
> ```
> > [!output]+
> >
> > ![[Pasted image 20250102212645.png]]
> >

>[!code]+ Данные одного столбца
>```py
> print(df['Salary'])
>```
>> [!output]+
>> ![[Pasted image 20250102212923.png]]

>[!code]+ Среднее значение данных столбца
>```py
> print(df['Salary'].mean())
>```
>>[!output]+
>>```py
>> 85.0
>>```