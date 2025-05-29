---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CompositeNode LastChild, чтобы легко получать доступ к последнему дочернему узлу и управлять им, улучшая управление структурой данных.
type: docs
weight: 50
url: /ru/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Получает последний дочерний элемент узла.

```csharp
public Node LastChild { get; }
```

## Примечания

Если нет последнего дочернего узла,`нулевой` возвращается.

## Примеры

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

// Удалить раздел на основе его родственных связей с другим разделом.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Раздел, который мы удалили, был первым, оставив в документе только второй.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Смотрите также

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
