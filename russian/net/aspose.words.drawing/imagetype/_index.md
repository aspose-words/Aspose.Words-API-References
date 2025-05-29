---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.ImageType для простого управления форматами изображений в документах Microsoft Word. Улучшите визуальную привлекательность вашего документа!
type: docs
weight: 1410
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
| Unknown | `1` | Неизвестный тип изображения или тип изображения, который невозможно напрямую сохранить в документе Microsoft Word. |
| Emf | `2` | Расширенный метафайл Windows. |
| Wmf | `3` | Метафайл Windows. |
| Pict | `4` | Macintosh PICT. Существующее изображение будет сохранено в документе, но вставка новых изображений PICT в документ не поддерживается. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Переносимая сетевая графика. |
| Bmp | `7` | Windows Bitmap. |
| Eps | `8` | Инкапсулированный PostScript. |
| WebP | `9` | ВебП. |
| Gif | `10` | GIF |

## Примеры

Показывает, как читать изображения WebP.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Показывает, как добавить изображение к фигуре и проверить его тип.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### Смотрите также

* property [ImageType](../imagedata/imagetype/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
