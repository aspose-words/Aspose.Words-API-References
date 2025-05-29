---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words für .NET
description: Passen Sie die Eigenschaft „ForegroundTintAndShade“ an, um Ihre Designfarben mühelos aufzuhellen oder abzudunkeln und so die visuelle Attraktivität Ihres Designs zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der eine Vordergrunddesignfarbe aufhellt oder abdunkelt.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 gesetzt wird. |
| InvalidOperationException | Wird ausgelöst, wenn diese Eigenschaft für das Schattierungsobjekt mit Nicht-Designfarben festgelegt ist. |

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (dunkelster Wert) bis 1 (hellster Wert).

Null (0) ist neutral.

## Beispiele

Zeigt, wie Vordergrund- und Hintergrundfarben für die Schattierungstextur festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### Siehe auch

* class [Shading](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
