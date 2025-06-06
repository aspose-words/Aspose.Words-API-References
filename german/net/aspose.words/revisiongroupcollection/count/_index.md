---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Count-Eigenschaft der RevisionGroupCollection. Rufen Sie einfach die Gesamtzahl der Revisionsgruppen ab und steigern Sie so die Effizienz Ihres Datenmanagements.
type: docs
weight: 10
url: /de/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Gibt die Anzahl der Revisionsgruppen in der Sammlung zurück.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie Informationen zu einer Gruppe von Revisionen in einem Dokument gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Siehe auch

* class [RevisionGroupCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
