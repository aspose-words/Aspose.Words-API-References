---
title: Class DownsampleOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.DownsampleOptions сорт. Позволяет указать параметры понижения разрешения.
type: docs
weight: 4970
url: /ru/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Позволяет указать параметры понижения разрешения.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) статья документации.

```csharp
public class DownsampleOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Указывает, следует ли понижать разрешение изображений. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Указывает разрешение в пикселях на дюйм, до которого изображения должны быть уменьшены. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения разрешения не будет применяться. Значение 0 означает, что проверка порога не используется и все изображения, могут быть уменьшены в размере. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


