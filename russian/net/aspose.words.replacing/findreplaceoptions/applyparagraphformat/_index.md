---
title: FindReplaceOptions.ApplyParagraphFormat
linktitle: ApplyParagraphFormat
articleTitle: ApplyParagraphFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ApplyParagraphFormat в FindReplaceOptions для бесшовного форматирования абзацев в ваших документах. Улучшайте свой контент без усилий!
type: docs
weight: 30
url: /ru/net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

Форматирование абзаца применено к новому содержимому.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

## Примеры

Показывает, как добавить форматирование к абзацам, в которых операция поиска и замены нашла совпадения.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите свойство "Alignment" на "ParagraphAlignment.Right", чтобы выровнять каждый абзац по правому краю
// содержащий совпадение, которое находит операция поиска и замены.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Замените каждую точку перед разрывом абзаца восклицательным знаком.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Смотрите также

* class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
