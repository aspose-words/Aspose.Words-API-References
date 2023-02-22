---
title: PsSaveOptions.UseBookFoldPrintingSettings
second_title: Справочник по API Aspose.Words для .NET
description: PsSaveOptions свойство. Получает или задает логическое значение указывающее следует ли сохранять документ с использованием макета печати брошюры  если он указан черезMultiplePages .
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати брошюры, , если он указан через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Примечания

Если указан этот параметр,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если в параметрах страницы не указаны параметры печати сгибом книги, этот параметр не будет действовать.

### Примеры

Показывает, как сохранить документ в формате Postscript в виде книжной складки.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект "PsSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в PostScript.
// Установите для свойства «UseBookFoldPrintingSettings» значение «true», чтобы упорядочить содержимое
// в выходном документе Postscript таким образом, чтобы мы могли сделать из него буклет.
// Установите для свойства "UseBookFoldPrintingSettings" значение "false", чтобы сохранить документ в обычном режиме.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Если мы визуализируем документ как буклет, мы должны установить «Несколько страниц»
// свойства объектов настройки страницы всех разделов на "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Как только мы напечатаем этот документ на обеих сторонах страниц, мы можем согнуть все страницы посередине одновременно,
// и содержимое выстроится таким образом, что получится буклет.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Смотрите также

* class [PsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pssaveoptions/)
* сборка [Aspose.Words](../../../)


