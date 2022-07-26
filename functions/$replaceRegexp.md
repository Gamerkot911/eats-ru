# $replaceRegexp
Замените что-нибудь с помощью RegExp.

### параметры:
| название          | тип        | описание                         | не обязательно? |
| ------------- | ----------- | ----------------------------------- | -------- |
| текст          | текст      | Номер для исправления, например: 4.124212     | ложь    |
| регулярное выражение        | текст      | Строка регулярного выражения.                  | ложь    |
| флаг          | RegExp-flag | The regexp flag.                    | false    |
| replacement   | String      | Anything to replace that regexp.    | false    |

### Example:
```js
$replaceRegexp[$get[text];/[^a-zA-Z0-9]/;g;] // Hello  what are u doing
$var[text;Hello $ #what are u doing!]
```
