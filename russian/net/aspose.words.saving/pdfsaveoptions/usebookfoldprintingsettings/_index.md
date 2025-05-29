---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions UseBookFoldPrintingSettings, позволяющее легко сохранять документы в виде брошюры для повышения эффективности печати.
type: docs
weight: 320
url: /ru/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Возвращает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, , если он указан через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Примечания

Если указана эта опция,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если параметры печати сгиба книги не указаны в параметрах страницы, этот параметр не будет иметь никакого эффекта.

## Примеры

Показывает, как сохранить документ в формате PDF в виде книжного сгиба.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "UseBookFoldPrintingSettings" в значение "true", чтобы упорядочить содержимое
// в выходном PDF-файле таким образом, чтобы его можно было использовать для создания буклета.
// Установите свойство «UseBookFoldPrintingSettings» в значение «false» для обычного отображения PDF-файла.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Если мы визуализируем документ как брошюру, мы должны установить "MultiplePages"
// свойства объектов настройки страницы всех разделов на "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// После того, как мы распечатаем этот документ с обеих сторон страниц, мы можем сложить все страницы посередине одновременно,
// и содержимое будет выстроено таким образом, что получится брошюра.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
