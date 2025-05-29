---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ZoomFactor в PdfSaveOptions, позволяющее легко настраивать уровни масштабирования документа в процентах, что улучшит ваши впечатления от просмотра PDF-файлов.
type: docs
weight: 360
url: /ru/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Возвращает или задает значение, определяющее коэффициент масштабирования (в процентах) для документа.

```csharp
public int ZoomFactor { get; set; }
```

## Примечания

Это значение используется только если[`ZoomBehavior`](../zoombehavior/) установлен наZoomFactor .

## Примеры

Показывает, как установить масштабирование по умолчанию, которое читатель применяет при открытии визуализированного PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
// Установите свойство "ZoomBehavior" на "PdfZoomBehavior.ZoomFactor", чтобы программа чтения PDF-файлов
// применяем процентный коэффициент масштабирования при открытии документа.
// Установите свойство «ZoomFactor» на «25», чтобы задать коэффициент масштабирования 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Когда мы откроем этот документ с помощью программы для чтения, например Adobe Acrobat, мы увидим документ, масштабированный в 1/4 от его фактического размера.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
