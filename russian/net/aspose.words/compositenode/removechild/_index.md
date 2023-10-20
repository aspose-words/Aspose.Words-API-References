---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words для .NET
description: CompositeNode RemoveChild метод. Удаляет указанный дочерний узел на С#.
type: docs
weight: 170
url: /ru/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

Удаляет указанный дочерний узел.

```csharp
public Node RemoveChild(Node oldChild)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| oldChild | Node | Узел, который нужно удалить. |

### Возвращаемое значение

Удаленный узел.

## Примечания

Родитель*oldChild* установлено на`нулевой` после удаления узла.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
