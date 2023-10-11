---
title: RevisionGroup.Text
second_title: Aspose.Words for .NET API Referansı
description: RevisionGroup mülk. Eklenen/silinen/taşınan metni veya biçim değişikliğinin açıklamasını döndürür.
type: docs
weight: 30
url: /tr/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Eklenen/silinen/taşınan metni veya biçim değişikliğinin açıklamasını döndürür.

```csharp
public string Text { get; }
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

* class [RevisionGroup](../)
* ad alanı [Aspose.Words](../../revisiongroup/)
* toplantı [Aspose.Words](../../../)


