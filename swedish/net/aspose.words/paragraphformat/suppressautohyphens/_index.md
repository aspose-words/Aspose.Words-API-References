---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words för .NET
description: ParagraphFormat SuppressAutoHyphens fast egendom. Anger om det aktuella stycket ska undantas från avstavning som används i dokumentinställningarna i C#.
type: docs
weight: 370
url: /sv/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Anger om det aktuella stycket ska undantas från avstavning som används i dokumentinställningarna.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Exempel

Visar hur man undertrycker avstavning för ett stycke.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öppna ett dokument som innehåller text med ett språk som matchar vår ordbok.
// När vi sparar det här dokumentet till ett fast sidsparformat kommer dess text att ha avstavning.
Document doc = new Document(MyDir + "German text.docx");

// Vi kan ställa in egenskapen "SuppressAutoHyphens" till "true" för att inaktivera avstavning
// för ett specifikt stycke samtidigt som det hålls aktiverat för resten av dokumentet.
// Standardvärdet för den här egenskapen är "false",
// vilket innebär att varje stycke som standard använder avstavning om någon är tillgänglig.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
