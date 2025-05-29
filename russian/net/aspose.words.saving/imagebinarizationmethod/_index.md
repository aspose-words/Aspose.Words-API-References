---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.ImageBinarizationMethod для эффективной бинаризации изображений. Оптимизируйте обработку документов с помощью передовых методов.
type: docs
weight: 5950
url: /ru/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Указывает метод, используемый для бинаризации изображения.

```csharp
public enum ImageBinarizationMethod
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Threshold | `0` | Указывает пороговый метод. |
| FloydSteinbergDithering | `1` | Задает сглаживание с использованием метода диффузии ошибок Флойда-Стейнберга. |

## Примеры

Показывает, как установить порог ошибки бинаризации TIFF при использовании метода Флойда-Стейнберга для рендеринга изображения TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ как TIFF, мы можем передать объект SaveOptions
// настройте сглаживание, которое Aspose.Words будет применять при рендеринге этого изображения.
// Значение свойства "ThresholdForFloydSteinbergDithering" по умолчанию равно 128.
// Более высокие значения, как правило, приводят к получению более темных изображений.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
