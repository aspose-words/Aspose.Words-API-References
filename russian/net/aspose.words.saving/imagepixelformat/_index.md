---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.ImagePixelFormat для оптимальных форматов пикселей в изображениях страниц документов. Улучшайте визуальные эффекты документов без усилий!
type: docs
weight: 5970
url: /ru/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Задает формат пикселей для создаваемых изображений страниц документа.

```csharp
public enum ImagePixelFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 бит на пиксель, RGB. |
| Format16BppRgb565 | `1` | 16 бит на пиксель, RGB. |
| Format16BppArgb1555 | `2` | 16 бит на пиксель, ARGB. |
| Format24BppRgb | `3` | 24 бита на пиксель, RGB. |
| Format32BppRgb | `4` | 32 бита на пиксель, RGB. |
| Format32BppArgb | `5` | 32 бита на пиксель, ARGB. |
| Format32BppPArgb | `6` | 32 бита на пиксель, ARGB, предварительно умноженная альфа. |
| Format48BppRgb | `7` | 48 бит на пиксель, RGB. |
| Format64BppArgb | `8` | 64 бита на пиксель, ARGB. |
| Format64BppPArgb | `9` | 64 бита на пиксель, ARGB, предварительно умноженная альфа. |
| Format1bppIndexed | `10` | 1 бит на пиксель, индексированный. |

## Примеры

Показывает, как выбрать скорость передачи бит на пиксель для преобразования документа в изображение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions
// выберите формат пикселей для изображения, которое будет сгенерировано при операции сохранения.
// Различные скорости передачи бит на пиксель влияют на качество и размер файла сгенерированного изображения.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Мы можем клонировать экземпляры ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
