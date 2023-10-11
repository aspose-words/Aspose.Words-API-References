---
title: Shading.BackgroundTintAndShade
second_title: Aspose.Words für .NET-API-Referenz
description: Shading eigendom. Ruft einen DoubleWert ab oder legt diesen fest der die Hintergrundfarbe eines Themas aufhellt oder abdunkelt.
type: docs
weight: 30
url: /de/net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

Ruft einen Double-Wert ab oder legt diesen fest, der die Hintergrundfarbe eines Themas aufhellt oder abdunkelt.

```csharp
public double BackgroundTintAndShade { get; set; }
```

### Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder mehr als 1 festzulegen, führt zuArgumentOutOfRangeException.

Das Festlegen dieser Eigenschaft für ein Schattierungsobjekt mit Nicht-Theme-Farben führt zuInvalidOperationException.

### Beispiele

Zeigt, wie man Vordergrund- und Hintergrundfarben für die Schattierungstextur festlegt.

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
* namensraum [Aspose.Words](../../shading/)
* Montage [Aspose.Words](../../../)


