---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ParagraphFormat WordWrap påverkar textbrytning i Word. Lär dig att styra textflödet på latin för förbättrad läsbarhet i dokumentet.
type: docs
weight: 420
url: /sv/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Om den här egenskapen är`falsk` , Latinsk text mitt i ett ord kan radbrytas för det aktuella stycket. Annars radbryts latinsk text av hela ord.

```csharp
public bool WordWrap { get; set; }
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
