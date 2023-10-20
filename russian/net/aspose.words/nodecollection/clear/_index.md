---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: NodeCollection Clear метод. Удаляет все узлы из этой коллекции и из документа на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Удаляет все узлы из этой коллекции и из документа.

```csharp
public void Clear()
```

## Примеры

Показывает, как удалить все разделы из документа.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Этот документ имеет один раздел с несколькими дочерними узлами, содержащими и отображающими все содержимое документа.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Очистка коллекции разделов, при этом будут удалены все дочерние элементы документа.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Смотрите также

* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
