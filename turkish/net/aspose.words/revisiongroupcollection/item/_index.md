---
title: RevisionGroupCollection.Item
second_title: Aspose.Words for .NET API Referansı
description: RevisionGroupCollection mülk. Belirtilen dizinde bir revizyon grubu döndürür.
type: docs
weight: 20
url: /tr/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Belirtilen dizinde bir revizyon grubu döndürür.

```csharp
public RevisionGroup this[int index] { get; }
```

### Örnekler

Bir belgede bir grup düzeltmenin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Ayrıca bakınız

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* ad alanı [Aspose.Words](../../revisiongroupcollection/)
* toplantı [Aspose.Words](../../../)


