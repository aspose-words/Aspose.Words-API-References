---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: Aspose.Words для .NET
description: Узнайте, как свойство TxtSaveOptions AddBidiMarks улучшает экспорт обычного текста, добавляя двунаправленные метки для улучшения читаемости и форматирования.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Указывает, следует ли добавлять двунаправленные метки перед каждым запуском BiDi при экспорте в формате обычного текста.

Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Примеры

Показывает, как вставить символ Unicode «ЗНАК СПРАВА НАЛЕВО» (U+200F) перед каждым двунаправленным символом Run в тексте.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Создаем объект "TxtSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ сохранения документа в виде обычного текста.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Установите свойство "AddBidiMarks" в значение "true", чтобы добавлять отметки перед забегами
// с текстом, написанным справа налево, для обозначения факта.
// Установите свойство "AddBidiMarks" в значение "false", чтобы писать все слева направо
// и справа налево выполняются одинаково, и ничто не указывает, что есть что.
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
