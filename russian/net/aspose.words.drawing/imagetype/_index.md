---
title: Enum ImageType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.ImageType перечисление. Указывает тип формат изображения в документе Microsoft Word.
type: docs
weight: 950
url: /ru/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Указывает тип (формат) изображения в документе Microsoft Word.

```csharp
public enum ImageType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| NoImage | `0` | Нет данных изображения. |
| Unknown | `1` | Неизвестный тип изображения или тип изображения, который нельзя напрямую сохранить в документе Microsoft Word. |
| Emf | `2` | Расширенный метафайл Windows. |
| Wmf | `3` | Метафайл Windows. |
| Pict | `4` | Macintosh ИЗОБРАЖЕНИЕ. Существующее изображение будет сохранено в документе, но вставка новых изображений PICT в документ не поддерживается. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Портативная сетевая графика. |
| Bmp | `7` | Растровое изображение Windows. |

### Примеры

Показывает, как добавить изображение к фигуре и проверить ее тип.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // Изображение в URL имеет формат .gif. Вставка его в документ преобразует его в .png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Смотрите также

* property [ImageType](../imagedata/imagetype/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


