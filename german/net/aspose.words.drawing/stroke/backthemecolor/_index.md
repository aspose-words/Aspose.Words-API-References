---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words für .NET
description: Passen Sie Ihr Design mit der Eigenschaft „Stroke BackThemeColor“ an. Legen Sie einfach eine Themenfarbe für Ihren Strichhintergrund fest, um die visuelle Attraktivität zu steigern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Strichhintergrundfarbe darstellt.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

## Beispiele

Zeigt, wie Sie die Designfarbe sowie den Farbton und die Schattierung zurücksetzen.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Siehe auch

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
