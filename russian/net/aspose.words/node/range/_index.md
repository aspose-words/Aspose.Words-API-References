---
title: Node.Range
second_title: Справочник по API Aspose.Words для .NET
description: Node свойство. Возвращает Диапазон объект представляющий часть документа содержащегося в этом узле.
type: docs
weight: 80
url: /ru/net/aspose.words/node/range/
---
## Node.Range property

Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле.

```csharp
public Range Range { get; }
```

### Примеры

Показывает, как удалить все узлы из диапазона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем текст в первый раздел документа, а затем добавляем еще один раздел.
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
* пространство имен [Aspose.Words](../../node/)
* сборка [Aspose.Words](../../../)


