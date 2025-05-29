---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Оптимизируйте свой контент с помощью метода EnsureMinimum, гарантируя, что каждый раздел будет включать в себя основную часть с абзацем для большей ясности и структуры.
type: docs
weight: 150
url: /ru/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Гарантирует, что раздел имеет[`Body`](../body/) с одним[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Примеры

Показывает, как подготовить новый узел раздела для редактирования.

```csharp
Document doc = new Document();

// Пустой документ содержит раздел, в котором есть тело, в котором, в свою очередь, есть абзац.
// Мы можем добавить содержимое в этот документ, добавив в этот абзац такие элементы, как текстовые строки, фигуры или таблицы.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Если мы добавим новый раздел, подобный этому, у него не будет тела или каких-либо других дочерних узлов.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Запустите метод «EnsureMinimum», чтобы добавить текст и абзац в этот раздел и начать его редактирование.
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
