---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: RevisionGroupCollection Item mülk. Belirtilen dizindeki revizyon grubunu döndürür C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Belirtilen dizindeki revizyon grubunu döndürür.

```csharp
public RevisionGroup this[int index] { get; }
```

## Örnekler

Bir belgede bir grup revizyonun nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Ayrıca bakınız

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
