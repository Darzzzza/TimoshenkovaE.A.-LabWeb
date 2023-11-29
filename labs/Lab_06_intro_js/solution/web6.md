﻿# Введение JavaScript
___________________________________________________
## Лабораторная работа №6
***Тимошенкова Е.А. [АСБ-3-036]***
___________________________________________________
### Ответы на вопросы:

**Через какой оператор Вы объявили переменую?**
- Переменная была объявлена через оператор "var".

**Какие доступны операторы для объявления переменных? В чём их отличия?**
- Операторы для объявления переменных в JavaScript включают "var", "let" и "const". 
- Отличия между ними заключаются в области видимости и возможности переопределения значений.

**Что происходит при вызове alert()?**
- Функция alert(), отображает модальное диалоговое окно с указанным сообщением, предназначенное для уведомления пользователя.

**Как Вы думаете для чего может использоваться console.log()**
- Функция console.log() используется для вывода информации в консоль разработчика браузера.

### Код:
```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>JS</title>
</head>
<body>
    <script class="Task 1">
        let apple = 10;
        let condition = ''

        alert(apple);
        console.log(apple);

        for (let i = 0; i < 5; i ++) {
            condition += String.fromCharCode(97 + Math.floor(Math.random() * 26))
        }

        console.log('Good game is ' + condition);
    </script>

    <script class="Task 2">
        let someInt = Math.floor(Math.random() * 100)
        let someText = '100'
        let someBool = true

        console.log(someInt + someText + someBool);
        console.log(someBool + someInt + someText);
        console.log(someText + someBool + someInt);
        console.log(someBool + someText + someInt);
        console.log(someInt + someBool + someText);
        console.log(someText + someInt + someBool);
    </script>

    <script class="Task 3">
        let array = new Array(10)

        for (let i = 0; i < array.length; i++) {
            array[i] = -10 + Math.floor(Math.random() * 20)
        }

        console.log('Old = ', array);

        array = array.filter(num => num > 0)

        console.log('New = ', array);
    </script>

    <script class="Task 4">

        function randomNum(min, max) {
            return Math.floor(min + Math.random() * (max + 1 - min));
        }


        function arrayMultiply(array, num) {
            return array.map(arrayNum => arrayNum * num);
        }

        function randomText() {
            for (let i = 0; i < 11; i++)
                condition += String.fromCharCode(97 + Math.floor(Math.random() * 26))
            return condition
        }

        console.log(randomNum(-10, 10));
        console.log(arrayMultiply([1, 20, 11, -3, 6], 10));
        console.log(randomText());
    </script>

    <script class="Task 5">
        let Obj = {
            firstName: 'Alina',
            surname: 'Lovina',
            patronymic: 'Sergeevich',
            birthday: new Date('1999-05-18'),
            hobby: 'English',
            group: 'Gudy',
            info: function() {
                return 'Имя: ' + this.firstName + '\nФамилия: ' + this.surname + '\nОтчество: '
                + this.patronymic + '\nХобби: ' + this.hobby + '\nВозраст: ' + (new Date().getFullYear() - this.birthday.getFullYear())
            }
        }

        alert(Obj.info())

        let salaryObj = {
            "Ivanov": 20000,
            "Petrov": 25000,
            "Sidorov": 30000,
            "Kozlov": 18000,
            "Smirnov": 22000,
            "Ofin": 28000,
            "Vasiliev": 24000,
            "Popov": 27000,
            "Fokin": 21000,
            "Sherban": 26000,
        }

        sumSalary = Object.values(salaryObj).reduce((a, b) => a + b, 0)

        console.log(sumSalary);
    </script>
</body>
</html>
```

### Результат:
![](img/6(1).png)
![](img/6(2).png)
![](img/6(3).png)
![](img/6(4).png)