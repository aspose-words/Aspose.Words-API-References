---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: .NET için Aspose.Words
description: Belge yönetimi ve işleme yeteneklerinizi geliştirerek Alt Belge verilerini verimli bir şekilde döndüren Alt Belge NodeType özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

Geri DöndürürSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## Örnekler

Ana belgenin alt belgelerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Bu düğüm harici bir belgeye referans görevi görür ve içeriğine erişilemez.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Ayrıca bakınız

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
