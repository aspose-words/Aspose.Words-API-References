---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SubDocument NodeType, которое эффективно возвращает данные SubDocument, расширяя возможности управления и обработки документов.
type: docs
weight: 10
url: /ru/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

ВозвратSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## Примеры

Показывает, как получить доступ к поддокументу главного документа.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Этот узел служит ссылкой на внешний документ, и его содержимое недоступно.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Смотрите также

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
