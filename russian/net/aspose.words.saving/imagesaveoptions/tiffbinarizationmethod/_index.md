---
title: ImageSaveOptions.TiffBinarizationMethod
linktitle: TiffBinarizationMethod
articleTitle: TiffBinarizationMethod
second_title: Aspose.Words для .NET
description: ImageSaveOptions TiffBinarizationMethod свойство. Получает или задает метод используемый при преобразовании изображений в формат 1 бит/пиксель  когдаSaveFormat являетсяTiff and TiffCompression равноCcitt3 илиCcitt4  на С#.
type: docs
weight: 170
url: /ru/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Получает или задает метод, используемый при преобразовании изображений в формат 1 бит/пиксель , когда[`SaveFormat`](../saveformat/) являетсяTiff and [`TiffCompression`](../tiffcompression/) равноCcitt3 илиCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

## Примечания

Значение по умолчанию:Threshold.

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

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
