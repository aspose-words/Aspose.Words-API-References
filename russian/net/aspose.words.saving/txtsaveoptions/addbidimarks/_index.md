---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: Aspose.Words для .NET
description: TxtSaveOptions AddBidiMarks свойство. Указывает добавлять ли двунаправленные метки перед каждым запуском двунаправленного текста при экспорте в текстовом формате на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Указывает, добавлять ли двунаправленные метки перед каждым запуском двунаправленного текста при экспорте в текстовом формате.

Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Примеры

Показывает, как вставить символ Юникода «Знак справа налево» (U+200F) перед каждым двунаправленным вводом текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Создаем объект «TxtSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Установите для свойства «AddBidiMarks» значение «true», чтобы добавлять метки перед запуском
// с текстом, написанным справа налево, чтобы указать факт.
// Установите для свойства «AddBidiMarks» значение «false», чтобы писать все слева направо
// и справа налево выполняются одинаково, без указания того, что есть что.
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### Смотрите также

* class [TxtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
