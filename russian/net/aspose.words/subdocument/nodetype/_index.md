---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words для .NET
description: SubDocument NodeType свойство. ВозвращаетSubDocument  на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

ВозвращаетSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## Примеры

Показывает, как получить доступ к вложенному документу составного документа.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Этот узел служит ссылкой на внешний документ, и к его содержимому невозможно получить доступ.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Смотрите также

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
