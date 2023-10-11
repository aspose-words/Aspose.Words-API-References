---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
second_title: Справочник по API Aspose.Words для .NET
description: ImportFormatOptions свойство. Получает или задает логическое значение указывающее следует ли автоматически регулировать интервал между предложениями и словами. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 20
url: /ru/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Получает или задает логическое значение, указывающее, следует ли автоматически регулировать интервал между предложениями и словами. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

### Примеры

Показывает, как автоматически регулировать интервал между предложениями и словами.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Смотрите также

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../importformatoptions/)
* сборка [Aspose.Words](../../../)


