---
title: PdfSaveOptions.DownsampleOptions
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Позволяет указать параметры понижения разрешения.
type: docs
weight: 100
url: /ru/net/aspose.words.saving/pdfsaveoptions/downsampleoptions/
---
## PdfSaveOptions.DownsampleOptions property

Позволяет указать параметры понижения разрешения.

```csharp
public DownsampleOptions DownsampleOptions { get; set; }
```

### Примеры

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

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


