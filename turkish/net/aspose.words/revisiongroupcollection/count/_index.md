---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: RevisionGroupCollection'ın Count özelliğini keşfedin. Toplam revizyon grubu sayısını kolayca alın, veri yönetimi verimliliğinizi artırın.
type: docs
weight: 10
url: /tr/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Koleksiyondaki revizyon gruplarının sayısını döndürür.

```csharp
public int Count { get; }
```

## Örnekler

Bir belgedeki revizyon grubuyla ilgili bilgilerin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Ayrıca bakınız

* class [RevisionGroupCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
