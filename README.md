# API для Yatube

### Описание проекта
**Yatube - социальная сеть**, в которой пользователи могут:
- Просматривать посты, опубликованные разными авторами
- Зарегистрироваться, что бы получить возможность публиковать свой контент
- Публиковать свои посты, можно даже с картинками
- Подписываться на других авторов и следить за их постами
- Делиться мнением о посте в комментариях
- Создавать группы по интересам и приписывать посты к этим группам

**Для этого проекта я реализовал REST API**. Оно вынесено в отдельное приложение и реализовано для всех моделей (Посты, группы, комментарии, подписки). Аутентифицированный пользователь авторизован на изменение и удаление своего контента; в остальных случаях доступ предоставляется только для чтения.

### Как локально развернуть проект?
- Клонируйте репозиторий
- Создайте и активируйте виртуальное окружение
- Установите все необходимые пакеты из requirements.txt
- Запустите сервер

Вы так же можете **изучить документацию:** http://127.0.0.1:8000/redoc/

### Примеры запросов
Получить список постов:
```bash 
GET /api/v1/posts/
```
Опубликовать новый пост (необходима авторизация):
```bash
POST /api/v1/posts/

{
    "text": "New post text",
    "image": "image.jpg"
}
```
Изменить конкретный пост (необходима авторизация):
```bash
PUT /api/v1/posts/<post_id>/

{
    "text": "Updated post text",
    "image": "new_image.jpg"
}
```
Удалить конкретный пост (необходима авторизация):
```bash
DELETE /api/v1/posts/<post_id>/
```



### Автор: Муратов Максим
Backend Python Developer
