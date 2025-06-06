---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: .NET için Aspose.Words
description: Gelişmiş düzenleme ve işbirliği için belge revizyon gruplarının etkili yönetimini sağlayan Aspose.Words.RevisionGroupCollection sınıfını keşfedin.
type: docs
weight: 5530
url: /tr/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Bir koleksiyon[`RevisionGroup`](../revisiongroup/)belgedeki revizyon gruplarını temsil eden nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgedeki Değişiklikleri İzle](https://docs.aspose.com/words/net/track-changes-in-a-document/) belgeleme makalesi.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Koleksiyondaki revizyon gruplarının sayısını döndürür. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Belirtilen dizinde bir revizyon grubu döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Şunu kullanın:[`Groups`](../revisioncollection/groups/) Bir belgede bulunan revizyon gruplarını almak için özelliği.

## Örnekler

Bir belgedeki revizyon grubunun nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
