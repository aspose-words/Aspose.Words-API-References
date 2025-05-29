---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words für .NET
description: Entdecken Sie Range Revisions. Verfolgen und verwalten Sie Eigenschaftsänderungen mühelos mit unserer umfassenden Sammlung von Revisionen für mehr Projektübersicht.
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

Bei der zurückgegebenen Sammlung handelt es sich um eine „Live“-Sammlung. Das bedeutet, wenn Sie Teile eines Dokuments entfernen, die Revisionen enthalten, verschwinden die gelöschten Revisionen automatisch aus dieser Sammlung.

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

// Die ersten Abschnittsrevisionen ablehnen.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Siehe auch

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
