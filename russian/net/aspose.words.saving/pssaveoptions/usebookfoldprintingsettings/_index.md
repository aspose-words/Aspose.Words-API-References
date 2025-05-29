---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PsSaveOptions UseBookFoldPrintingSettings, позволяющее легко сохранять документы в виде брошюры для повышения эффективности печати.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Возвращает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, , если он указан через[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Примечания

Если указана эта опция,[`PageSet`](../../fixedpagesaveoptions/pageset/) игнорируется при сохранении. Это поведение соответствует MS Word. Если параметры печати сгиба книги не указаны в параметрах страницы, этот параметр не будет иметь никакого эффекта.

## Примеры

Показывает, как сохранить документ в формате Postscript в виде книжного сгиба.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект "PsSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в PostScript.
// Установите свойство "UseBookFoldPrintingSettings" в значение "true", чтобы упорядочить содержимое
// в выходном документе Postscript таким образом, чтобы это помогло нам сделать из него брошюру.
// Установите свойство «UseBookFoldPrintingSettings» в значение «false», чтобы сохранить документ обычным образом.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Если мы визуализируем документ как брошюру, мы должны установить "MultiplePages"
// свойства объектов настройки страницы всех разделов на "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// После того, как мы распечатаем этот документ с обеих сторон страниц, мы можем сложить все страницы посередине одновременно,
// и содержимое будет выстроено таким образом, что получится брошюра.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Смотрите также

* class [PsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
