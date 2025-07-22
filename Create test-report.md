# Звіт з виконання тестів JMeter до JSONPlaceholder

## Налаштування
- 5 типів запитів: GET, POST, PUT, PATCH, DELETE
- Виконання: 3 ітерації протягом 10 секунд
- Всі запити на сервер: https://jsonplaceholder.typicode.com

## Результати
- ✅ GET /posts/1 → 200 OK, валідна відповідь з полем title
- ✅ POST /posts → 201 Created, відповідь містить id, userId, title
- ✅ PUT /posts/1 → 200 OK, оновлене поле title
- ✅ PATCH /posts/1 → 200 OK, часткове оновлення
- ✅ DELETE /posts/1 → 200 OK, порожня відповідь {}

## Висновки
- Сервіс JSONPlaceholder стабільно обробляє CRUD-запити
- Усі перевірки (Response Code, Text Contains, JSON Path) виконані успішно
- DELETE не має тіла, тому JSON Assertion не застосовувався

## Listener'и
- View Results Tree — дозволив побачити тіла відповідей
- Summary Report — підтвердив час виконання та кількість ітерацій
