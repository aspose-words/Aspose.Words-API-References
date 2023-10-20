---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words för .NET
description: Fill ForeTintAndShade fast egendom. Hämtar eller ställer in ett dubbelt värde som gör förgrundsfärgen ljusare eller mörkare i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Hämtar eller ställer in ett dubbelt värde som gör förgrundsfärgen ljusare eller mörkare.

```csharp
public double ForeTintAndShade { get; set; }
```

## Anmärkningar

De tillåtna värdena ligger inom intervallet från -1 (den mörkaste) till 1 (den ljusaste) för den här egenskapen. Noll (0) är neutral. Ett försök att ställa in den här egenskapen till ett värde mindre än -1 eller mer än 1 resulterar iArgumentOutOfRangeException.

## Exempel

Visar hur man hanterar ljusare och mörkare teckensnittsfärger i förgrunden.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
