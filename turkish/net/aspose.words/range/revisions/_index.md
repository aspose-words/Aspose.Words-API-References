---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: .NET için Aspose.Words
description: Range Revizyonlarını keşfedin. Proje netliğini artırmak için kapsamlı revizyon koleksiyonumuzla mülk değişikliklerini zahmetsizce takip edin ve yönetin.
type: docs
weight: 40
url: /tr/net/aspose.words/range/revisions/
---
## Range.Revisions property

Bu aralıkta bulunan revizyonların (izlenen değişikliklerin) bir koleksiyonunu alır.

```csharp
public RevisionCollection Revisions { get; }
```

## Notlar

Döndürülen koleksiyon "canlı" bir koleksiyondur; bu, bir belgenin revizyon içeren kısımlarını kaldırırsanız, silinen revizyonların bu koleksiyondan otomatik olarak kaybolacağı anlamına gelir.

## Örnekler

Aralıktaki revizyonlarla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// İlk bölüm revizyonlarını reddedin.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Ayrıca bakınız

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
