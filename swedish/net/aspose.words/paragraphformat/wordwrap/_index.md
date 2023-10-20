---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words för .NET
description: ParagraphFormat WordWrap fast egendom. Om den här egenskapen ärfalsk  latinsk text i mitten av ett ord kan lindas för det aktuella stycket. Annars är latinsk text omsluten av hela ord i C#.
type: docs
weight: 410
url: /sv/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Om den här egenskapen är`falsk` , latinsk text i mitten av ett ord kan lindas för det aktuella stycket. Annars är latinsk text omsluten av hela ord.

```csharp
public bool WordWrap { get; set; }
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
