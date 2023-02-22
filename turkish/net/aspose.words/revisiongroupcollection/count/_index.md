---
title: RevisionGroupCollection.Count
second_title: Aspose.Words for .NET API Referansı
description: RevisionGroupCollection mülk. Koleksiyondaki revizyon gruplarının sayısını verir.
type: docs
weight: 10
url: /tr/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Koleksiyondaki revizyon gruplarının sayısını verir.

```csharp
public int Count { get; }
```

### Örnekler

Bir belgedeki bir grup düzeltme hakkındaki bilgilerin nasıl yazdırılacağını gösterir.

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
* ad alanı [Aspose.Words](../../revisiongroupcollection/)
* toplantı [Aspose.Words](../../../)


