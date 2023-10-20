---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words для .NET
description: XpsSaveOptions UseBookFoldPrintingSettings свойство. Получает или задает логическое значение указывающее следует ли сохранять документ с использованием макета для печати буклета  если оно указано черезMultiplePages  на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета для печати буклета, , если оно указано через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Примечания

Если указана эта опция,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если параметры печати сгиба книги не указаны в настройках страницы, этот параметр не будет иметь никакого эффекта.

## Примеры

Показывает, как сохранить документ в формате XPS в виде сгиба книги.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект «XpsSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в документ .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Установите для свойства UseBookFoldPrintingSettings значение «true», чтобы упорядочить содержимое
// в выходном файле XPS таким образом, чтобы его можно было использовать для создания буклета.
// Установите для свойства UseBookFoldPrintingSettings значение «false», чтобы нормально отображать XPS.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Если мы отображаем документ как буклет, мы должны установить «MultiplePages»
// свойства объектов настройки страницы всех разделов равны "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Распечатав этот документ, мы можем превратить его в буклет, сложив страницы стопкой
// выйти из принтера и сложить посередине.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Смотрите также

* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
