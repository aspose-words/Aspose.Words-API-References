---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words для .NET
description: Управляйте CompositeNode без усилий с помощью метода RemoveChild, разработанного для упрощения удаления узлов с целью повышения производительности и эффективности.
type: docs
weight: 190
url: /ru/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

Удаляет указанный дочерний узел.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| oldChild | T | Узел, который необходимо удалить. |

### Возвращаемое значение

Удаленный узел.

## Примечания

Родитель*oldChild* установлен на`нулевой` после удаления узла.

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
