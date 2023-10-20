---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words для .NET
description: CompositeNode IndexOf метод. Возвращает индекс указанного дочернего узла в массиве дочерних узлов на С#.
type: docs
weight: 120
url: /ru/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Возвращает индекс указанного дочернего узла в массиве дочерних узлов.

```csharp
public int IndexOf(Node child)
```

## Примечания

Возвращает -1, если узел не найден среди дочерних узлов.

## Примеры

Показывает, как получить индекс данного дочернего узла от его родительского узла.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Получаем индекс последнего абзаца тела первого раздела.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Смотрите также

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
