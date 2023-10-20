---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Section EnsureMinimum метод. Гарантирует что в разделе естьBody с однимParagraph  на С#.
type: docs
weight: 130
url: /ru/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Гарантирует, что в разделе есть[`Body`](../body/) с одним[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Примеры

Показывает, как подготовить новый узел раздела к редактированию.

```csharp
Document doc = new Document();

// Пустой документ имеет раздел, в котором есть тело, которое, в свою очередь, имеет абзац.
// Мы можем добавить содержимое в этот документ, добавив в этот абзац такие элементы, как текстовые фрагменты, фигуры или таблицы.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Если мы добавим новый раздел таким образом, у него не будет тела или других дочерних узлов.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Запускаем метод EnsureMinimum, чтобы добавить тело и абзац в этот раздел и начать его редактирование.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
