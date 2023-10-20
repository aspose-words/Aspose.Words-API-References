---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words для .NET
description: PdfSaveOptions UseBookFoldPrintingSettings свойство. Получает или задает логическое значение указывающее следует ли сохранять документ с использованием макета для печати буклета  если оно указано черезMultiplePages  на С#.
type: docs
weight: 300
url: /ru/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета для печати буклета, , если оно указано через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Примечания

Если указана эта опция,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если параметры печати сгиба книги не указаны в настройках страницы, этот параметр не будет иметь никакого эффекта.

## Примеры

Показывает, как сохранить документ в формате PDF в виде книжного сгиба.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства UseBookFoldPrintingSettings значение «true», чтобы упорядочить содержимое
// в выходном PDF-файле таким образом, чтобы его можно было использовать для создания буклета.
// Установите для свойства UseBookFoldPrintingSettings значение «false», чтобы нормально отобразить PDF-файл.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Если мы отображаем документ как буклет, мы должны установить «MultiplePages»
// свойства объектов настройки страницы всех разделов равны "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Как только мы напечатаем этот документ на обеих сторонах страниц, мы сможем сразу сложить все страницы посередине,
// и содержимое выстроится в линию, образующую буклет.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
