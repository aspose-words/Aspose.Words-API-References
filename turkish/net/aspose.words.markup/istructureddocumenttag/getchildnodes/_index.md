---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: .NET için Aspose.Words
description: IStructuredDocumentTag GetChildNodes metodunu keşfedin, gelişmiş belge yönetimi için belirttiğiniz türlere göre uyarlanmış dinamik bir alt düğüm koleksiyonuna erişin.
type: docs
weight: 170
url: /tr/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## Örnekler

Yapılandırılmış belge etiketinin nasıl kaldırılacağını gösterir, ancak içeriği içeride tutar.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Bu koleksiyon, aralıklı ve aralıksız yapılandırılmış etiketlere erişim için birleşik bir arayüz sağlar.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Burada, aralıklı ve aralıksız yapılandırılmış etiketlerin ortak arayüzünden alt düğümleri alabiliriz.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Ayrıca bakınız

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
