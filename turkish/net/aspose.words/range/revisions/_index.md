---
title: Range.Revisions
second_title: Aspose.Words for .NET API Referansı
description: Range mülk. Bu aralıkta mevcut olan revizyonların izlenen değişiklikler bir koleksiyonunu alır.
type: docs
weight: 40
url: /tr/net/aspose.words/range/revisions/
---
## Range.Revisions property

Bu aralıkta mevcut olan revizyonların (izlenen değişiklikler) bir koleksiyonunu alır.

```csharp
public RevisionCollection Revisions { get; }
```

### Notlar

Döndürülen koleksiyon "canlı" bir koleksiyondur; yani bir belgenin düzeltmelerini içeren bölümlerini kaldırırsanız, silinen düzeltmeler bu koleksiyondan otomatik olarak kaybolacaktır.

### Örnekler

Aralıktaki revizyonlarla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// İlk bölüm revizyonlarını reddet.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Ayrıca bakınız

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* ad alanı [Aspose.Words](../../range/)
* toplantı [Aspose.Words](../../../)


