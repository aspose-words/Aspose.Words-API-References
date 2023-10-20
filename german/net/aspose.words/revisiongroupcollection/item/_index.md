---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: RevisionGroupCollection Item eigendom. Gibt eine Revisionsgruppe am angegebenen Index zurück in C#.
type: docs
weight: 20
url: /de/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Gibt eine Revisionsgruppe am angegebenen Index zurück.

```csharp
public RevisionGroup this[int index] { get; }
```

## Beispiele

Zeigt, wie eine Gruppe von Revisionen in einem Dokument abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Siehe auch

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
