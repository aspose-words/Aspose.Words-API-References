---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words för .NET
description: Upptäck intervallrevideringar. Spåra och hantera fastighetsändringar enkelt med vår omfattande samling av revisioner för förbättrad projekttydlighet.
type: docs
weight: 40
url: /sv/net/aspose.words/range/revisions/
---
## Range.Revisions property

Hämtar en samling revisioner (spårade ändringar) som finns inom detta intervall.

```csharp
public RevisionCollection Revisions { get; }
```

## Anmärkningar

Den returnerade samlingen är en "live"-samling, vilket innebär att om du tar bort delar av ett dokument som innehåller -revisioner, kommer de borttagna revisionerna automatiskt att försvinna från samlingen.

## Exempel

Visar hur man arbetar med revisioner inom intervallet.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Avvisa de första avsnittsrevideringarna.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Se även

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
