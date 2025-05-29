---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words för .NET
description: Kontrollera avstavning i ditt dokument med egenskapen ParagraphFormat SuppressAutoHyphens, vilket säkerställer tydlig och professionell styckeformatering.
type: docs
weight: 380
url: /sv/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Anger om det aktuella stycket ska undantas från bindestreck som används i dokumentinställningarna.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Exempel

Visar hur man undertrycker bindestreck i ett stycke.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öppna ett dokument som innehåller text med en språkinställning som matchar vår ordlista.
// När vi sparar det här dokumentet i ett fast sidformat kommer texten att ha bindestreck.
Document doc = new Document(MyDir + "German text.docx");

// Vi kan ställa in egenskapen "SuppressAutoHyphens" till "true" för att inaktivera bindestreck
// för ett specifikt stycke medan det är aktiverat för resten av dokumentet.
// Standardvärdet för den här egenskapen är "falskt",
// vilket innebär att varje stycke som standard använder bindestreck om sådant finns tillgängligt.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
