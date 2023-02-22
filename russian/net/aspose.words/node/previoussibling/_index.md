---
title: Node.PreviousSibling
second_title: Справочник по API Aspose.Words для .NET
description: Node свойство. Получает узел непосредственно предшествующий этому узлу.
type: docs
weight: 70
url: /ru/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Получает узел, непосредственно предшествующий этому узлу.

```csharp
public Node PreviousSibling { get; }
```

### Примечания

Если предыдущего узла нет, возвращается null.

### Примеры

Показывает, как использовать методы Node и CompositeNode для удаления раздела перед последним разделом в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Оба раздела являются родственными друг другу.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Удаляем раздел на основе родственного отношения с другим разделом.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Раздел, который мы удалили, был первым, оставив в документе только второй.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Смотрите также

* class [Node](../)
* пространство имен [Aspose.Words](../../node/)
* сборка [Aspose.Words](../../../)


