---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words för .NET
description: Få åtkomst till och anpassa fotnots- och slutnotsavgränsare i ditt dokument med DocumentBases egenskap FootnoteSeparators för förbättrad formateringskontroll.
type: docs
weight: 40
url: /sv/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Ger åtkomst till fotnots-/slutnotsavgränsare som definierats i dokumentet.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

## Exempel

Visar hur man tar bort slutnotsavgränsaren.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Ta bort slutnotsavgränsare.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Visar hur man hanterar formatet för fotnotsavgränsare.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Justera fotnotsavgränsaren.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Se även

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
