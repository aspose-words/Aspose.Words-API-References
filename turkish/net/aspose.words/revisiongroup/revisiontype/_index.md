---
title: RevisionGroup.RevisionType
second_title: Aspose.Words for .NET API Referansı
description: RevisionGroup mülk. Bu gruba dahil olan revizyonların türünü alır.
type: docs
weight: 20
url: /tr/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Bu gruba dahil olan revizyonların türünü alır.

```csharp
public RevisionType RevisionType { get; }
```

### Örnekler

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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* ad alanı [Aspose.Words](../../revisiongroup/)
* toplantı [Aspose.Words](../../../)


