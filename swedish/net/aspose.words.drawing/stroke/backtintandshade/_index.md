---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words för .NET
description: Justera din bakgrundsfärg enkelt med Stroke BackTintAndShade. Kontrollera ljusstyrka och mörkhet för en perfekt designfinish.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp linjens bakgrundsfärg.

```csharp
public double BackTintAndShade { get; set; }
```

## Anmärkningar

De tillåtna värdena ligger inom intervallet från -1 (mörkast) till 1 (ljusast) för den här egenskapen. Noll (0) är neutralt. Om du försöker ställa in den här egenskapen till ett värde mindre än -1 eller mer än 1 resulterar det iArgumentOutOfRangeException.

## Exempel

Visar hur man återställer temafärg, nyans och skugga.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Se även

* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
