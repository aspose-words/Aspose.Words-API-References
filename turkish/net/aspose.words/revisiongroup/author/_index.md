---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: .NET için Aspose.Words
description: Her revizyon grubunun yazarını kolayca belirlemek için RevisionGroup Author özelliğini keşfedin ve belge yönetimi verimliliğinizi artırın.
type: docs
weight: 10
url: /tr/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Bu revizyon grubunun yazarını alır.

```csharp
public string Author { get; }
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

* class [RevisionGroup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
