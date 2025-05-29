---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: .NET için Aspose.Words
description: AdvancedCompareOptions IgnoreStoreItemId özelliğinin, daha iyi doğruluk için StructuredDocumentTag Kimlik farklılıklarını yok sayarak belge karşılaştırmasını nasıl geliştirdiğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

StructuredDocumentTag depolama öğesi kimliğindeki farkın göz ardı edilip edilmeyeceğini belirtir.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## Notlar

Varsayılan değer`YANLIŞ` .

## Örnekler

Aynı içeriğe sahip ancak farklı mağaza öğesi kimliğine sahip SDT'nin nasıl karşılaştırılacağını gösterir.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Aynı içeriğe sahip ancak farklı mağaza öğesi kimliğine sahip SDT'yi karşılaştırmak için seçenekleri yapılandırın.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Ayrıca bakınız

* class [AdvancedCompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../../)
