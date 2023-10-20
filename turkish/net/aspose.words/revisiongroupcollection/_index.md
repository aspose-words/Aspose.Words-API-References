---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.RevisionGroupCollection sınıf. Bir koleksiyonRevisionGroup belgedeki revizyon gruplarını temsil eden nesneler C#'da.
type: docs
weight: 4790
url: /tr/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Bir koleksiyon[`RevisionGroup`](../revisiongroup/) belgedeki revizyon gruplarını temsil eden nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgedeki Değişiklikleri İzleme](https://docs.aspose.com/words/net/track-changes-in-a-document/) dokümantasyon makalesi.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Koleksiyondaki revizyon gruplarının sayısını döndürür. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Belirtilen dizindeki revizyon grubunu döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Kullan[`Groups`](../revisioncollection/groups/) Bir belgede revizyon gruplarının bulunmasını sağlayan özelliği.

## Örnekler

Bir belgede bir grup revizyonun nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
