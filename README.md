### [Python](http://wiki.cs.hse.ru/Основы_и_методология_программирования_на_ПМИ_2018/2019_(основной_поток,_1_модуль))


* [Download book/lectures](https://disk.yandex.ru/i/BkcKilJkumcPV)
* [Online lectures](https://www.coursera.org/learn/python-osnovy-programmirovaniya/home/welcome)

#### Week 1
0. - [x] [PEP 8 - Руководство по стилю для кода Python](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/0.md)
1. - [x] [Введение](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/1.md)

#### Week 2
2. - [x] [Условный оператор](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/2.md)
3. - [ ] [Цикл While](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/3.md)

### Tasks
0. - [ ] [Nim Game](https://leetcode.com/problems/nim-game/)
1. - [ ] [Reverse Integer](https://leetcode.com/problems/reverse-integer/)
2. - [ ] [Add Binary](https://leetcode.com/problems/add-binary/)
3. - [ ] [sqrt(x)](https://leetcode.com/problems/sqrtx/)
4. - [ ] [Multiply strings](https://leetcode.com/problems/multiply-strings/)
5. - [ ] [Roman to integer](https://leetcode.com/problems/roman-to-integer/)

#### Week 3
4. - [ ] [Строки](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/4.md)
5. - [ ] [Функция](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/5.md)

#### Week 4
6. - [ ] [Цикл for](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/6.md)
7. - [ ] [Списки - List](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/7.md)

#### Week 5
8. - [ ] [Сортировка](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/8.md)
9. - [ ] [Множество - Set](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/9.md)

#### Week 6
10. - [ ] [Словарь - Dictionary](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/10.md)
11. - [ ] [Функциональное программирование](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/11.md)

12. - [ ] [Класс](https://github.com/doroteo7/HSE-Python-1/blob/master/notes/12.md)




 


#### Чтение файла построчно в Python

```python
infile = open('input.txt')

data = infile.readlines()

for row in data:
    a = list(row.split())

infile.close()
```
