---
title: PsSaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: PsSaveOptions свойство. Указывает формат в котором документ будет сохранен если используется этот объект параметров сохранения. Может быть толькоPs .
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Указывает формат, в котором документ будет сохранен, если используется этот объект параметров сохранения. Может быть толькоPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pssaveoptions/)
* сборка [Aspose.Words](../../../)


