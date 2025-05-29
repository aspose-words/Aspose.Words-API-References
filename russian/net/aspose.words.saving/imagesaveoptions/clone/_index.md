---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words для .NET
description: Откройте для себя метод клонирования ImageSaveOptions, позволяющий без труда создавать глубокие клоны ваших объектов, повышая эффективность и гибкость кодирования.
type: docs
weight: 210
url: /ru/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Создает глубокую копию этого объекта.

```csharp
public ImageSaveOptions Clone()
```

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

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
