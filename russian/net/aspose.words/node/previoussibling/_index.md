---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words для .NET
description: Node PreviousSibling свойство. Получает узел непосредственно предшествующий этому узлу на С#.
type: docs
weight: 70
url: /ru/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Получает узел, непосредственно предшествующий этому узлу.

```csharp
public Node PreviousSibling { get; }
```

## Примечания

Если предыдущего узла нет,`нулевой` возвращается.

## Примеры

Показывает, как использовать методы Node и CompositeNode для удаления раздела перед последним разделом в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Обе секции являются родственными друг другу.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Удаление раздела на основе его родственных отношений с другим разделом.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Раздел, который мы удалили, был первым, оставив в документе только второй.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Смотрите также

* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
