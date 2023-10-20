---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words для .NET
description: PdfSaveOptions ZoomBehavior свойство. Получает или задает значение определяющее какой тип масштабирования следует применять при открытии документа с помощью средства просмотра PDF на С#.
type: docs
weight: 320
url: /ru/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Получает или задает значение, определяющее, какой тип масштабирования следует применять при открытии документа с помощью средства просмотра PDF.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Примечания

Значение по умолчанию:None , т. е. подгонка не применяется.

## Примеры

Показывает, как установить масштабирование по умолчанию, которое программа чтения применяет при открытии обработанного PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
// Установите для свойства «ZoomBehavior» значение «PdfZoomBehavior.ZoomFactor», чтобы программа чтения PDF-файлов могла
// применяем коэффициент масштабирования в процентах, когда мы открываем с ним документ.
// Установите для свойства ZoomFactor значение «25», чтобы присвоить коэффициенту масштабирования значение 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Когда мы откроем этот документ с помощью программы чтения, например Adobe Acrobat, мы увидим документ, масштабированный в 1/4 от его фактического размера.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Смотрите также

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
