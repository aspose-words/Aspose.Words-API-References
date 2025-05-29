---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Footnote ActualReferenceMark för att få åtkomst till den exakta texten i referensmarkeringar i dina dokument, vilket förbättrar tydlighet och organisation.
type: docs
weight: 20
url: /sv/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Hämtar den faktiska texten för referensmärket som visas i dokumentet för denna fotnot.

```csharp
public string ActualReferenceMark { get; }
```

## Anmärkningar

För att initialt fylla i värden för den här egenskapen för alla referensmärken i dokumentet, eller för att uppdatera värdena efter ändringar i dokumentet som kan påverka referensmärkena, måste du köra [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) method. Uppdaterar fält ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) kan också vara nödvändigt för att få rätt resultat.

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

* class [Footnote](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
