---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words для .NET
description: Node Range свойство. ВозвращаетRange объект представляющий часть документа содержащуюся в этом узле на С#.
type: docs
weight: 80
url: /ru/net/aspose.words/node/range/
---
## Node.Range property

Возвращает[`Range`](../../range/) объект, представляющий часть документа, содержащуюся в этом узле.

```csharp
public Range Range { get; }
```

## Примеры

Показывает, как удалить все узлы из диапазона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем текст в первый раздел документа, а затем добавляем еще один раздел.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Полностью удаляем первый раздел, удалив все узлы
// в пределах своего диапазона, включая сам раздел.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Смотрите также

* class [Range](../../range/)
* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
