> [!info]+ Импорт библиотеки
> ```py
> import matplotlib.pyplot as plt
> # pyplot - модуль, отвечающий за построение графиков
> # plt - псевдоним (можно выбрать любой)
> ```

# Графики

>[!code]+
> ```py
> import matplotlib.pyplot as plt
> 
> # Координаты:
> x = [70,80,100,150,300]
> y = [1,4,6,9,16]
> 
> plt.plot(x,y)
> plt.title('Уровень дохода и счастья') # Заголовок
> plt.xlabel('Доход') # Заголовок по Ox
> plt.ylabel('Уровень счастья') # Заголовок по Oy
> plt.show() # Вывод графика
> ```
>> [!output]+
>> ![[Pasted image 20250102211341.png]]

Графики можно накладывать друг на друга

> [!code]+
> ```py
> plt.plot(x,y) # Синий график
> plt.plot([39,50,80,100,200,300],[1,4,7,9,18,22]) # Оранжевый график
> plt.title('Уровень дохода и счастья')
> plt.xlabel('Доход')
> plt.ylabel('Уровень счастья')
> plt.show()
> ```
> > [!output]+
> > ![[Pasted image 20250102211638.png]]

---
# Диаграммы


> [!code]+
> ```py
> import matplotlib.pyplot as plt
> 
> year = ['First', 'Second', 'Third', 'Fourth', 'Fifth']
> frequency = [500, 470, 300, 260, 220]
> 
> plt.bar(year, frequency) # Диаграмма
> plt.xlabel('Курс')
> plt.ylabel('Кол-во студентов')
> plt.title('Распределение студентов по курсам университета')
> plt.show()
> ```
> > [!output]+
> >  ![[Pasted image 20250102215456.png]]



