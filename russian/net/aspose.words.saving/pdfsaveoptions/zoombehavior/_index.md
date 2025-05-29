---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words для .NET
description: Откройте для себя PdfSaveOptions ZoomBehavior, управляйте настройками масштабирования для оптимального просмотра в программах просмотра PDF. Улучшите пользовательский опыт с помощью индивидуального отображения документов!
type: docs
weight: 350
url: /ru/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Возвращает или задает значение, определяющее, какой тип масштабирования следует применять при открытии документа с помощью средства просмотра PDF-файлов.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Примечания

Значение по умолчанию:None , т.е. подгонка не применяется.

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
