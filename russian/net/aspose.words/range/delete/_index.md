---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words для .NET
description: Range Delete метод. Удаляет все символы диапазона на С#.
type: docs
weight: 70
url: /ru/net/aspose.words/range/delete/
---
## Range.Delete method

Удаляет все символы диапазона.

```csharp
public void Delete()
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

* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
