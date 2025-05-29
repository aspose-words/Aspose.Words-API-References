---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft RevisionGroup RevisionType, um die Revisionstypen in Ihrem Projekt einfach zu identifizieren und zu verwalten. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 20
url: /de/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Ruft den Typ der in dieser Gruppe enthaltenen Revisionen ab.

```csharp
public RevisionType RevisionType { get; }
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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
