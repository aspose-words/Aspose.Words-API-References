---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words для .NET
description: DownsampleOptions Resolution свойство. Указывает разрешение в пикселях на дюйм до которого изображения должны быть уменьшены на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Указывает разрешение в пикселях на дюйм, до которого изображения должны быть уменьшены.

```csharp
public int Resolution { get; set; }
```

## Примечания

Значение по умолчанию — 220 пикселей на дюйм.

## Примеры

Показывает, как изменить разрешение изображений в документе PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// По умолчанию Aspose.Words снижает разрешение всех изображений в документе, который мы сохраняем в PDF, до 220 пикселей на дюйм.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Установите для свойства «Разрешение» значение «36», чтобы уменьшить разрешение всех изображений до 36 пикселей на дюйм.
options.DownsampleOptions.Resolution = 36;

// Установите свойство «ResolutionThreshold», чтобы применить понижающую дискретизацию только к
// изображения с разрешением выше 128 пикселей на дюйм.
options.DownsampleOptions.ResolutionThreshold = 128;

// На этом этапе будут уменьшены только первые два изображения из документа.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Смотрите также

* class [DownsampleOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
