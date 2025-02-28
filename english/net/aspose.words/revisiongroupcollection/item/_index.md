---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access specific revision groups effortlessly with the RevisionGroupCollection Item property. Enhance your data management with precise indexing.
type: docs
weight: 20
url: /net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Returns a revision group at the specified index.

```csharp
public RevisionGroup this[int index] { get; }
```

## Examples

Shows how to get a group of revisions in a document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### See Also

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
