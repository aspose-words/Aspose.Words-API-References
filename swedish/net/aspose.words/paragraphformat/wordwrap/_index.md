---
title: ParagraphFormat.WordWrap
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Om den här egenskapen är falsk latinsk text i mitten av ett ord kan lindas för det aktuella stycket. Annars är latinsk text omsluten av hela ord.
type: docs
weight: 400
url: /sv/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Om den här egenskapen är **falsk** latinsk text i mitten av ett ord kan lindas för det aktuella stycket. Annars är latinsk text omsluten av hela ord.

```csharp
public bool WordWrap { get; set; }
```

### Exempel

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
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


