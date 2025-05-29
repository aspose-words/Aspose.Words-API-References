---
title: DownsampleOptions.ResolutionThreshold
linktitle: ResolutionThreshold
articleTitle: ResolutionThreshold
second_title: Aspose.Words для .NET
description: Оптимизируйте свои изображения с помощью свойства DownsampleOptions ResolutionThreshold. Управляйте понижением разрешения на основе разрешения для лучшей производительности и качества.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения разрешения не будет применен. Значение 0 означает, что проверка порогового значения не используется, и все изображения, размер которых можно уменьшить, подвергаются понижению разрешения.

```csharp
public int ResolutionThreshold { get; set; }
```

## Примечания

Значение по умолчанию — 0.

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
