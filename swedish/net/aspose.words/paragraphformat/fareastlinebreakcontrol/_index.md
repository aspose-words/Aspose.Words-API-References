---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat FarEastLineBreakControl, som aktiverar östasiatiska radbrytningsregler för exakt textformatering i dina dokument.
type: docs
weight: 110
url: /sv/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Hämtar eller anger en flagga som anger om östasiatiska radbrytningsregler tillämpas på det aktuella stycket.

```csharp
public bool FarEastLineBreakControl { get; set; }
```

## Exempel

Visar hur man ställer in specialegenskaper för asiatisk typografi.

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
