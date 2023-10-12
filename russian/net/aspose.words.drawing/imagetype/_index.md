---
title: Enum ImageType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.ImageType перечисление. Указывает тип формат изображения в документе Microsoft Word.
type: docs
weight: 1080
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
| Unknown | `1` | Неизвестный тип изображения или тип изображения, который нельзя сохранить непосредственно в документе Microsoft Word. |
| Emf | `2` | Расширенный метафайл Windows. |
| Wmf | `3` | Метафайл Windows. |
| Pict | `4` | Macintosh ИЗОБРАЖЕНИЕ. Существующее изображение будет сохранено в документе, но вставка изображений new PICT в документ не поддерживается. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Портативная сетевая графика. |
| Bmp | `7` | Растровое изображение Windows. |
| Eps | `8` | Инкапсулированный PostScript. |

### Примеры

Показывает, как добавить изображение в фигуру и проверить его тип.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // Изображение в URL-адресе имеет формат .gif. Вставка его в документ преобразует его в формат .png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Смотрите также

* property [ImageType](../imagedata/imagetype/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


