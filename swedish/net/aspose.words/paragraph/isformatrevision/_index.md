---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen IsFormatRevision i Microsoft Word spårar formateringsändringar, vilket säkerställer korrekta dokumentredigeringar och förbättrat samarbete.
type: docs
weight: 90
url: /sv/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Returnerar sant om objektets formatering ändrades i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsFormatRevision { get; }
```

## Exempel

Visar hur man kontrollerar om ett stycke är en formatrevision.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Detta stycke är en "Format"-revidering, vilket sker när vi ändrar formateringen av befintlig text.
// vid spårning av revisioner i Microsoft Word via "Granska" -> "Spåra ändringar".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
