# $deleteObjectKey
Удалить значение ключа из созданного объекта.

### параметры:
| название      | тип                | описание                        | не обязательно? |
| --------- | ------------------- | ---------------------------------- | -------- |
| название | текст              | Имя значения ключа, которое вы хотите удалить . | ложь |

### пример:
```js
$deleteObjectKey[hello] // удалит этот ключ из объекта, Final: { start: 'hiii' }
$setObjectKey[hello;hi]
$setObjectKey[start;hiii]
$createObject
```