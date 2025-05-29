---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.DownsampleOptions, чтобы легко настроить понижение разрешения изображения для оптимизации качества и производительности документа.
type: docs
weight: 5720
url: /ru/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Позволяет указать параметры понижения разрешения.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

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
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Указывает, следует ли уменьшать разрешение изображений. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Указывает разрешение в пикселях на дюйм, до которого следует уменьшить разрешение изображений. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения разрешения не будет применен. Значение 0 означает, что проверка порогового значения не используется, и все изображения, размер которых можно уменьшить, подвергаются понижению разрешения. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
