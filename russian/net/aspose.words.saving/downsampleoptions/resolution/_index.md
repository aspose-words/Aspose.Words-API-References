---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words для .NET
description: Оптимизируйте качество изображения с помощью свойства DownsampleOptions Resolution, определяющего идеальное количество пикселей на дюйм для превосходных результатов понижения разрешения.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Указывает разрешение в пикселях на дюйм, до которого следует уменьшить разрешение изображений.

```csharp
public int Resolution { get; set; }
```

## Примечания

Значение по умолчанию — 220 ppi.

## Примеры

Показывает, как изменить разрешение изображений в PDF-документе.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// По умолчанию Aspose.Words понижает разрешение всех изображений в документе, который мы сохраняем в формате PDF, до 220 ppi.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Установите свойство «Разрешение» на «36», чтобы понизить разрешение всех изображений до 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Установите свойство "ResolutionThreshold", чтобы применить понижение разрешения только к
// изображения с разрешением выше 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// На этом этапе будут уменьшены разрешения только первых двух изображений документа.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Смотрите также

* class [DownsampleOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
