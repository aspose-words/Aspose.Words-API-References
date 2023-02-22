---
title: Range.Delete
second_title: Справочник по API Aspose.Words для .NET
description: Range метод. Удаляет все символы диапазона.
type: docs
weight: 60
url: /ru/net/aspose.words/range/delete/
---
## Range.Delete method

Удаляет все символы диапазона.

```csharp
public void Delete()
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

* class [Range](../)
* пространство имен [Aspose.Words](../../range/)
* сборка [Aspose.Words](../../../)


