---
title: RevisionGroupCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: RevisionGroupCollection eigendom. Gibt eine Revisionsgruppe am angegebenen Index zurück.
type: docs
weight: 20
url: /de/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Gibt eine Revisionsgruppe am angegebenen Index zurück.

```csharp
public RevisionGroup this[int index] { get; }
```

### Beispiele

Zeigt, wie Sie eine Gruppe von Revisionen in einem Dokument erhalten.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Siehe auch

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namensraum [Aspose.Words](../../revisiongroupcollection/)
* Montage [Aspose.Words](../../../)


