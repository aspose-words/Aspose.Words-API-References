---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: .NET için Aspose.Words
description: Belge ağacınızdaki içeriğini koruyarak bir SDT düğümünü zahmetsizce kaldırmak için IStructuredDocumentTag RemoveSelfOnly yöntemini keşfedin.
type: docs
weight: 180
url: /tr/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Yalnızca bu SDT düğümünü kaldırır, ancak içeriğini belge ağacının içinde tutar.

```csharp
public void RemoveSelfOnly()
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

* interface [IStructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
