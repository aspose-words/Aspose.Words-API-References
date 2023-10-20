---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words für .NET
description: Range Revisions eigendom. Ruft eine Sammlung von Revisionen nachverfolgten Änderungen ab die in diesem Bereich vorhanden sind in C#.
type: docs
weight: 40
url: /de/net/aspose.words/range/revisions/
---
## Range.Revisions property

Ruft eine Sammlung von Revisionen (nachverfolgten Änderungen) ab, die in diesem Bereich vorhanden sind.

```csharp
public RevisionCollection Revisions { get; }
```

## Bemerkungen

Die zurückgegebene Sammlung ist eine „Live“-Sammlung. Das heißt, wenn Sie Teile eines Dokuments entfernen, die Revisionen enthalten, verschwinden die gelöschten Revisionen automatisch aus dieser Sammlung.

## Beispiele

Zeigt, wie mit Revisionen im Bereich gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Die Überarbeitungen des ersten Abschnitts ablehnen.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Siehe auch

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
