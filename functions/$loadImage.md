# $loadImage
Загружает изображение и сохраняет идентификатор в качестве идентификатора.

### параметры:
| название          | тип        | описание                           | не обязательно? |
| ------------- | ----------- | ------------------------------------- | -------- |
| индефикатор            | текст      | индефикатор изображения.                         | ложь    |
| тип          | тип      | тип (path \| link)                    | ложь    |
| путь          | текст      | URL изображения или путь в зависимости от типа. | ложь    |

### пример:
```js
$loadImage[myPathImg;path;./image.png] // для локального изображения.
$loadImage[myUrlImg;link;https://...] // для дистанционного изображения.
```
