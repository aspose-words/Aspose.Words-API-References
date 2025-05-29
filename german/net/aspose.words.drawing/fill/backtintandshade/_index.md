---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words für .NET
description: Passen Sie die Eigenschaft „BackTintAndShade“ an, um Ihre Hintergrundfarbe mühelos aufzuhellen oder abzudunkeln und so die visuelle Attraktivität und das Benutzererlebnis Ihres Designs zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der die Hintergrundfarbe aufhellt oder abdunkelt.

```csharp
public double BackTintAndShade { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 gesetzt wird. |

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (dunkelster Wert) bis 1 (hellster Wert).

Null (0) ist neutral.

## Beispiele

Zeigt, wie die Designfarbe für die Vordergrund-/Hintergrundformfarbe festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Hinweis: Verwenden Sie „BackThemeColor“ und „BackTintAndShade“ nicht zum Füllen der Schriftart.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
