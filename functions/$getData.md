# $getData
Получить значение свойства из объекта запроса json (если есть).

### параметры:
| название      | тип                | описание                        | не обязательно? |
| --------- | ------------------- | ---------------------------------- | -------- |
| пропорции | пропорция              | Свойство от объекта для получения значения. | ложь |

### пример:
```js
$getData[data.something] 
$request[...] // необходимо использовать эту функцию

// пример кода:
$send[$getData[data.translated]] // ответ: Bonjour le monde
$request[https://api.miduwu.ga/json/translate?source=auto&target=fr&text=Hello+world]
```

<br/>

__ __
<br/>
<br/>

  The link returned a json
```json
{
 "status": 200,
 "data": {
  "translated": "Bonjour le monde",
  "source": "en",
  "target": "fr"
 },
 "success": true
}
```
  Итак, вам нужно выбрать объект, а затем значение, например: 
```js
data.source //ответ: en
status // ответ: 200
```
