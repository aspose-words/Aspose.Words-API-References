---
title: Enum ImageBinarizationMethod
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.ImageBinarizationMethod перечисление. Указывает метод используемый для бинаризации изображения.
type: docs
weight: 5200
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
| Threshold | `0` | Определяет пороговый метод. |
| FloydSteinbergDithering | `1` | Определяет сглаживание с использованием метода диффузии ошибок Флойда-Стейнберга. |

### Примеры

Показывает, как установить порог ошибки бинаризации TIFF при использовании метода Флойда-Стейнберга для рендеринга изображения TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ в формате TIFF, мы можем передать объект SaveOptions в
// корректируем сглаживание, которое Aspose.Words будет применять при рендеринге этого изображения.
// Значение по умолчанию свойства ThresholdForFloydSteinbergDithering — 128.
// Более высокие значения приводят к более темным изображениям.
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


