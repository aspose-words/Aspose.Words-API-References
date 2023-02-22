---
title: FindReplaceOptions.ApplyParagraphFormat
second_title: Справочник по API Aspose.Words для .NET
description: FindReplaceOptions свойство. Форматирование абзаца применяется к новому содержимому.
type: docs
weight: 30
url: /ru/net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

Форматирование абзаца применяется к новому содержимому.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

### Примеры

Показывает, как добавить форматирование к абзацам, в которых операция поиска и замены обнаружила совпадения.

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

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для свойства "Выравнивание" значение "ParagraphAlignment.Right", чтобы выровнять каждый абзац по правому краю.
// который содержит совпадение, найденное операцией поиска и замены.
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
* пространство имен [Aspose.Words.Replacing](../../findreplaceoptions/)
* сборка [Aspose.Words](../../../)


