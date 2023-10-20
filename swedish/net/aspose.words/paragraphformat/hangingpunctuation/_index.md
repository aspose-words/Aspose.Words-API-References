---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words för .NET
description: ParagraphFormat HangingPunctuation fast egendom. Hämtar eller ställer in en flagga som indikerar om hängande interpunktion är aktiverad för det aktuella stycket i C#.
type: docs
weight: 130
url: /sv/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Hämtar eller ställer in en flagga som indikerar om hängande interpunktion är aktiverad för det aktuella stycket.

```csharp
public bool HangingPunctuation { get; set; }
```

## Exempel

Visar hur du ställer in speciella egenskaper för asiatisk typografi.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
