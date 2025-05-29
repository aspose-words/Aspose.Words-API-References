---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words för .NET
description: Optimera din textlayout med egenskapen ParagraphFormat BaselineAlignment, vilket ger exakt kontroll över teckensnittets vertikala placering för förbättrad läsbarhet.
type: docs
weight: 40
url: /sv/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Hämtar eller ställer in teckensnittens vertikala position på en rad.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Exempel

Visar hur man ställer in teckensnittens vertikala position på en rad.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Se även

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
