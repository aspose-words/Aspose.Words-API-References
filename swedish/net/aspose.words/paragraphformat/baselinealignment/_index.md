---
title: ParagraphFormat.BaselineAlignment
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Hämtar eller ställer in teckensnitt vertikalt på en linje.
type: docs
weight: 40
url: /sv/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Hämtar eller ställer in teckensnitt vertikalt på en linje.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

### Exempel

Visar hur du ställer in teckensnitt vertikalt på en linje.

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
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


