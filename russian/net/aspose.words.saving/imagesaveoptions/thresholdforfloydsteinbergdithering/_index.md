---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words для .NET
description: ImageSaveOptions ThresholdForFloydSteinbergDithering свойство. Получает или задает порог определяющий значение ошибки бинаризации в методе ФлойдаСтейнберга.  когдаImageBinarizationMethod являетсяFloydSteinbergDithering  на С#.
type: docs
weight: 160
url: /ru/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Получает или задает порог, определяющий значение ошибки бинаризации в методе Флойда-Стейнберга. , когда[`ImageBinarizationMethod`](../../imagebinarizationmethod/) являетсяFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## Примечания

Значение по умолчанию — 128.

## Примеры

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

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
