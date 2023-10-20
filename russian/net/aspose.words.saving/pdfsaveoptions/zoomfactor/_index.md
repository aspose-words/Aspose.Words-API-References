---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words для .NET
description: PdfSaveOptions ZoomFactor свойство. Получает или задает значение определяющее коэффициент масштабирования в процентах для документа на С#.
type: docs
weight: 330
url: /ru/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Получает или задает значение, определяющее коэффициент масштабирования (в процентах) для документа.

```csharp
public int ZoomFactor { get; set; }
```

## Примечания

Это значение используется только в том случае, если[`ZoomBehavior`](../zoombehavior/) установлено наZoomFactor .

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

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
