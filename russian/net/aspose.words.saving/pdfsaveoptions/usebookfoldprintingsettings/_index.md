---
title: PdfSaveOptions.UseBookFoldPrintingSettings
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или задает логическое значение указывающее следует ли сохранять документ с использованием макета печати брошюры  если он указан черезMultiplePages .
type: docs
weight: 270
url: /ru/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати брошюры, , если он указан через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Примечания

Если указан этот параметр,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если в параметрах страницы не указаны параметры печати сгибом книги, этот параметр не будет действовать.

### Примеры

Показывает, как сохранить документ в формате PDF в виде книжной складки.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства «UseBookFoldPrintingSettings» значение «true», чтобы упорядочить содержимое
// в выходном PDF-файле таким образом, чтобы мы могли использовать его для создания буклета.
// Задайте для свойства UseBookFoldPrintingSettings значение false, чтобы PDF отображался нормально.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Если мы визуализируем документ как буклет, мы должны установить «Несколько страниц»
// свойства объектов настройки страницы всех разделов на "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Как только мы напечатаем этот документ на обеих сторонах страниц, мы можем согнуть все страницы посередине одновременно,
// и содержимое выстроится таким образом, что получится буклет.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


