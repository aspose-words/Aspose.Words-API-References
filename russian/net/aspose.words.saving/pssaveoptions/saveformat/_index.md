---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PsSaveOptions SaveFormat, чтобы легко указать формат сохранения вашего документа. Оптимизируйте свой рабочий процесс с помощью гибких параметров сохранения!
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
