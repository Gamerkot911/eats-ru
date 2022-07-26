# Советы

Полезные советы для улучшения вашего опыта кодирования.

## обработчик

Загрузите маршруты с обработчиком.

**Пример (установка):**
```js
import { API } from "easy-api.ts";

const api = new API({...})

api.routes.load('./routes').then(() => {
    api.connect() // We're starting the API when the source is ready.
})
```

**пример (маршрут):**
```js
// path: './routes/../../../route.js'
module.exports = {
    path: '/endpoint/name',
    details: {
        description: 'Anything',
        more_X_keys: 'anything'
    },
    code: `
    $send[200;json;{
        success: true
    }]
    `
}
```

## использования базы данных.

Сохранение, получение и удаление переменных из базы данных.

**пример (настройка):**
```js
import { API } from "easy-api.ts";

const api = new API({
    port: process.env.PORT || 3000,
    database: {
        enabled: true, // VERY IMPORTANT TO ENABLE IT!!
        type: 'replit', // You can use: 'replit' | 'default' | 'mongo'
        // mongoUrl: '...'
    }
})

api.connect()
```

**Функции:**

`$deleteVar[var name]` [доки здесь.](functions/$deleteVar.md)

`$getVar[var name]` [доки здесь.](functions/$getVar.md)

`$setVar[var name;value]` [доки здесь.](functions/$setVar.md)

## Создание своей функции

Добавьте свою собственную функцию, используя класс `<API>.interpreter`.

**Пример:**
```js
import { API, FunctionBuilder, Utils } from "easy-api.ts";

const api = new API({...})

api.interpreter.addFunction({
    data: new FunctionBuilder()
    .setName('test'),
    code: async d => {
        const unpacked = d.unpack(d)
        if(!unpacked.inside) return Utils.Warn('Invalid inside provided in:', d.func)
        return {
            code: d.code.resolve(`${d.func}[${unpacked.inside}]`, unpacked.inside + '< was a test.')
        }
    }
})

api.connect()
```
