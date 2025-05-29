---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: С легкостью очистите NodeCollection с помощью нашего метода Clear, удалив все узлы как из коллекции, так и из документа для оптимальной производительности.
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

// Очищаем коллекцию разделов, что приведет к удалению всех дочерних элементов документа.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Смотрите также

* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
