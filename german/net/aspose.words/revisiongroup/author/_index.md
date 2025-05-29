---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „RevisionGroup Author“, um den Autor jeder Revisionsgruppe einfach zu identifizieren und so die Effizienz Ihres Dokumentenmanagements zu steigern.
type: docs
weight: 10
url: /de/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Ruft den Autor dieser Revisionsgruppe ab.

```csharp
public string Author { get; }
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

* class [RevisionGroup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
