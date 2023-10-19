---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words for .NET
description: Aspose.Words.RevisionGroup sınıf. Sıralı bir grup temsil ederRevision nesneler C#'da.
type: docs
weight: 4780
url: /tr/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Sıralı bir grup temsil eder[`Revision`](../revision/) nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgedeki Değişiklikleri İzleme](https://docs.aspose.com/words/net/track-changes-in-a-document/) dokümantasyon makalesi.

```csharp
public class RevisionGroup
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Bu revizyon grubunun yazarını döndürür. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Bu gruba dahil olan revizyonların türünü alır. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Eklenen/silinen/taşınan metni veya biçim değişikliğinin açıklamasını döndürür. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
