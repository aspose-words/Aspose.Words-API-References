---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words для .NET
description: Оптимизируйте свои изображения с помощью порога ImageSaveOptions для сглаживания Флойда-Стейнберга. Контролируйте ошибку бинаризации для получения потрясающих результатов при обработке изображений.
type: docs
weight: 160
url: /ru/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Возвращает или задает пороговое значение, определяющее значение ошибки бинаризации в методе Флойда-Стейнберга. когда[`ImageBinarizationMethod`](../../imagebinarizationmethod/) являетсяFloydSteinbergDithering .

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

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
