---
title: CompositeNode.LastChild
second_title: Справочник по API Aspose.Words для .NET
description: CompositeNode свойство. Получает последнего дочернего узла узла.
type: docs
weight: 50
url: /ru/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Получает последнего дочернего узла узла.

```csharp
public Node LastChild { get; }
```

### Примечания

Если последнего дочернего узла нет,`нулевой` возвращается.

### Примеры

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

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../compositenode/)
* сборка [Aspose.Words](../../../)


