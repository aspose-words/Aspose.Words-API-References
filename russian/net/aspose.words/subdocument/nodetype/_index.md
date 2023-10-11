---
title: SubDocument.NodeType
second_title: Справочник по API Aspose.Words для .NET
description: SubDocument свойство. ВозвращаетSubDocument .
type: docs
weight: 10
url: /ru/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

ВозвращаетSubDocument .

```csharp
public override NodeType NodeType { get; }
```

### Примеры

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
* пространство имен [Aspose.Words](../../subdocument/)
* сборка [Aspose.Words](../../../)


