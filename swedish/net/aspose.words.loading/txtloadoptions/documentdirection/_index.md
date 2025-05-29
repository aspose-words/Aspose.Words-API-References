---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TxtLoadOptions DocumentDirection för att enkelt ställa in dokumentriktning. Optimera din layout med standardinställningen LeftToRight!
type: docs
weight: 50
url: /sv/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Hämtar eller anger en dokumentriktning. Standardvärdet ärLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Exempel

Visar hur man identifierar textriktningen i klartextdokument.

```csharp
// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Sätt egenskapen "DocumentDirection" till "DocumentDirection.Auto" identifierar automatiskt
// riktningen för varje textstycke som Aspose.Words laddar från klartext.
// Varje styckes "Bidi"-egenskap lagrar dess riktning.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Identifiera hebreisk text som höger-till-vänster.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Identifiera engelsk text som höger-till-vänster.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Se även

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
