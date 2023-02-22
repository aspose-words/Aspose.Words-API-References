---
title: PsSaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: PsSaveOptions свойство. Определяет формат в котором документ будет сохранен если используется этот объект параметров сохранения.Ps .
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Определяет формат, в котором документ будет сохранен, если используется этот объект параметров сохранения.Ps .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pssaveoptions/)
* сборка [Aspose.Words](../../../)


