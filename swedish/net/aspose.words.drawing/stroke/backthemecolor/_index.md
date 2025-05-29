---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words för .NET
description: Anpassa din design med egenskapen Stroke BackThemeColor. Ställ enkelt in en ThemeColor för din linjebakgrund för att förbättra den visuella attraktionskraften.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Hämtar eller ställer in ett ThemeColor-objekt som representerar streckets bakgrundsfärg.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
