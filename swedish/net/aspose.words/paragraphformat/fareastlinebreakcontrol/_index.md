---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words för .NET
description: ParagraphFormat FarEastLineBreakControl fast egendom. Hämtar eller ställer in en flagga som indikerar om östasiatiska linjebrytande regler tillämpas på det aktuella stycket i C#.
type: docs
weight: 110
url: /sv/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Hämtar eller ställer in en flagga som indikerar om östasiatiska linjebrytande regler tillämpas på det aktuella stycket.

```csharp
public bool FarEastLineBreakControl { get; set; }
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
