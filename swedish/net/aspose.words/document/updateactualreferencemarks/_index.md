---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words för .NET
description: Uppdatera enkelt alla fotnoter och slutnoter i ditt dokument med metoden Document UpdateActualReferenceMarks, vilket förbättrar noggrannheten och effektiviteten.
type: docs
weight: 800
url: /sv/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Uppdaterar[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) egenskap för alla fotnoter och slutnoter i dokumentet.

```csharp
public void UpdateActualReferenceMarks()
```

## Anmärkningar

Uppdaterar fält ([`UpdateFields`](../updatefields/) ) kan vara nödvändigt för att få rätt resultat.

## Exempel

Visar hur man får en faktisk fotnotsreferens.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
