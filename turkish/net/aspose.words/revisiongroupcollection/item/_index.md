---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: RevisionGroupCollection Item özelliğiyle belirli revizyon gruplarına zahmetsizce erişin. Hassas indekslemeyle veri yönetiminizi geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Belirtilen dizinde bir revizyon grubu döndürür.

```csharp
public RevisionGroup this[int index] { get; }
```

## Örnekler

Bir belgedeki revizyon grubunun nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Ayrıca bakınız

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
