---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSaveOptions PixelFormat, чтобы легко настраивать формат пикселей создаваемых изображений для достижения оптимального качества и производительности.
type: docs
weight: 120
url: /ru/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Получает или задает формат пикселей для сгенерированных изображений.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Примечания

Это свойство действует только при сохранении в растровых форматах изображений.

Значение по умолчанию:Format32BppArgb.

Формат пикселей выходного изображения может отличаться от установленного значения из-за работы GDI+.

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

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
