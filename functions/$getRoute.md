# $getRoute
Получить свойство маршрута.

### параметры:
| название        | тип        | описание                          | не обязательно? |
| ----------- | ----------- | ------------------------------------ | -------- |
| пропорции    | текст      | Свойство от маршрута до получения.      | ложь    |

**Пример шаблона:**
```js
module.exports = {
    path: '/myendpoint',
    details: {
        description: 'This is my endpoint description lol',
        usage: '?text=String'
    },
    code: `...`
}
```

### пример:
```js
$getRoute[/myendpoint;path] // /myendpoint
$getRoute[/myendpoint;details.description] // This is my endpoint description lol
$getRoute[/myendpoint;details.usage] // ?text=String
```
