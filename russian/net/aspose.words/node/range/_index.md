---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Node Range, легко получите доступ к объекту Range, который определяет сегмент документа в вашем узле для улучшенного управления содержимым.
type: docs
weight: 80
url: /ru/net/aspose.words/node/range/
---
## Node.Range property

Возвращает[`Range`](../../range/)объект, представляющий часть документа, содержащуюся в этом узле.

```csharp
public Range Range { get; }
```

## Примеры

Показывает, как удалить все узлы из диапазона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте текст в первый раздел документа, а затем добавьте еще один раздел.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Полностью удалить первый раздел, удалив все узлы
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
