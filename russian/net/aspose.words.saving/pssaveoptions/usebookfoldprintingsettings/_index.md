---
title: PsSaveOptions.UseBookFoldPrintingSettings
second_title: Справочник по API Aspose.Words для .NET
description: PsSaveOptions свойство. Получает или задает логическое значение указывающее следует ли сохранять документ с использованием макета для печати буклета  если оно указано черезMultiplePages .
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета для печати буклета, , если оно указано через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Примечания

Если указана эта опция,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если параметры печати сгиба книги не указаны в настройках страницы, этот параметр не будет иметь никакого эффекта.

### Примеры

Показывает, как сохранить документ в формате Postscript в виде книжного сгиба.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект «PsSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в PostScript.
// Установите для свойства UseBookFoldPrintingSettings значение «true», чтобы упорядочить содержимое
// в выходном документе Postscript таким образом, чтобы можно было сделать из него буклет.
// Установите для свойства «UseBookFoldPrintingSettings» значение «false», чтобы сохранить документ в обычном режиме.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Если мы отображаем документ как буклет, мы должны установить «MultiplePages»
// свойства объектов настройки страницы всех разделов равны "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Как только мы напечатаем этот документ на обеих сторонах страниц, мы сможем сразу сложить все страницы посередине,
// и содержимое выстроится в линию, образующую буклет.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Смотрите также

* class [PsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pssaveoptions/)
* сборка [Aspose.Words](../../../)


