# $registerFont
Зарегистрируйте пользовательский шрифт из пути.

### параметры:
| название         | тип     | описание                         | не обязательно?    |
| ------------ | -------- | ---------------------------------- | ----------- |
| путь         | текст   | Расположение файла шрифта.            | ложь       |
| название (индефикатор)       | текст   | Название шрифтов для регистрации (имя) | ложь       |

> ⚠️: **Разрешенные форматы шрифтов: `.ttf`, `.otf`**

### пример:

```js
$drawText[...]
$font[30;Any name] // Теперь мы можем использовать его
$createCanvas[512;512]
$registerFont[Any name;./assets/myfont.ttf] // Мы регистрируем его с произвольным именем
```
