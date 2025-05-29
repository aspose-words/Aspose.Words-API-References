---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
linktitle: AdjustSentenceAndWordSpacing
articleTitle: AdjustSentenceAndWordSpacing
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImportFormatOptions AdjustSentenceAndWordSpacing. Легко управляйте автоматическим интервалом между предложениями и словами для улучшения ясности текста.
type: docs
weight: 20
url: /ru/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Возвращает или задает логическое значение, указывающее, следует ли автоматически корректировать интервалы между предложениями и словами. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

## Примеры

Показывает, как автоматически корректировать интервалы между предложениями и словами.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
