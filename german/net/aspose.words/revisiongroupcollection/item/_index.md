---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos auf bestimmte Revisionsgruppen zu – mit der Elementeigenschaft „RevisionGroupCollection“. Verbessern Sie Ihr Datenmanagement durch präzise Indizierung.
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

Zeigt, wie man eine Gruppe von Revisionen in einem Dokument erhält.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Siehe auch

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
