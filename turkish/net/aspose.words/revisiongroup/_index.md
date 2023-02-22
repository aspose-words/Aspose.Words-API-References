---
title: Class RevisionGroup
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.RevisionGroup sınıf. Bir grup sıralıRevision nesneler.
type: docs
weight: 4520
url: /tr/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Bir grup sıralı[`Revision`](../revision/) nesneler.

```csharp
public class RevisionGroup
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Bu revizyon grubunun yazarını alır. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Bu gruba dahil olan düzeltmelerin türünü alır. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Eklenen/silinen/taşınan metni veya biçim değişikliğinin açıklamasını döndürür. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


