---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: .NET için Aspose.Words
description: Sıralı Revision nesnelerini verimli bir şekilde yönetmek ve düzenlemek ve belge düzenlemeyi kolaylaştırmak için tasarlanmış Aspose.Words.RevisionGroup sınıfını keşfedin.
type: docs
weight: 5520
url: /tr/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Sıralı bir grup temsil eder[`Revision`](../revision/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgedeki Değişiklikleri İzle](https://docs.aspose.com/words/net/track-changes-in-a-document/) belgeleme makalesi.

```csharp
public class RevisionGroup
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Bu revizyon grubunun yazarını alır. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Bu gruba dahil edilen revizyonların türünü alır. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Eklenen/silinmiş/taşınan metni veya biçim değişikliğinin açıklamasını döndürür. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
