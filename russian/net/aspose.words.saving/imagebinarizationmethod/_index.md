---
title: ImageBinarizationMethod
second_title: Справочник по API Aspose.Words для .NET
description: Определяет метод используемый для бинаризации изображения.
type: docs
weight: 4940
url: /ru/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Определяет метод, используемый для бинаризации изображения.

```csharp
public enum ImageBinarizationMethod
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Threshold | `0` | Задает пороговый метод. |
| FloydSteinbergDithering | `1` | Задает сглаживание с использованием метода распространения ошибок Флойда-Стейнберга. |

### Примеры

Показывает, как установить порог ошибки бинаризации TIFF при использовании метода Флойда-Стейнберга для визуализации изображения TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ в формате TIFF, мы можем передать объект SaveOptions в
// настроить сглаживание, которое Aspose.Words будет применять при рендеринге этого изображения.
// Значение свойства ThresholdForFloydSteinbergDithering по умолчанию равно 128.
// Чем выше значение, тем темнее изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
