---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words для .NET
description: Оптимизируйте макет документа с помощью свойства XpsSaveOptions UseBookFoldPrintingSettings, обеспечивающего бесперебойную печать брошюр для улучшенной презентации.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Возвращает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, , если он указан через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Примечания

Если указана эта опция,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если параметры печати сгиба книги не указаны в параметрах страницы, этот параметр не будет иметь никакого эффекта.

## Примеры

Показывает, как сохранить документ в формате XPS в виде книжного сгиба.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект "XpsSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Установите свойство "UseBookFoldPrintingSettings" в значение "true", чтобы упорядочить содержимое
// в выходном XPS-файле таким образом, чтобы его можно было использовать для создания буклета.
// Установите свойство «UseBookFoldPrintingSettings» в значение «false» для обычной визуализации XPS.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Если мы визуализируем документ как брошюру, мы должны установить "MultiplePages"
// свойства объектов настройки страницы всех разделов на "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// После того, как мы распечатаем этот документ, мы можем превратить его в брошюру, сложив страницы
// чтобы вынуть из принтера и сложить пополам.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Смотрите также

* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
