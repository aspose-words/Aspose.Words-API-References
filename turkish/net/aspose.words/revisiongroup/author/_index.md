---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words for .NET
description: RevisionGroup Author mülk. Bu revizyon grubunun yazarını döndürür C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Bu revizyon grubunun yazarını döndürür.

```csharp
public string Author { get; }
```

## Örnekler

Bir belgedeki revizyon grubu hakkındaki bilgilerin nasıl yazdırılacağını gösterir.

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

* class [RevisionGroup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
