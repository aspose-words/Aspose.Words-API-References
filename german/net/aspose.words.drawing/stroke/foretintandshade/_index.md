---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words für .NET
description: Passen Sie die Eigenschaft „Stroke ForeTintAndShade“ an, um die Vordergrundfarbe Ihres Strichs mühelos aufzuhellen oder abzudunkeln und so die visuelle Wirkung zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der die Vordergrundfarbe des Strichs aufhellt oder abdunkelt.

```csharp
public double ForeTintAndShade { get; set; }
```

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (dunkelster Wert) bis 1 (hellster Wert). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 zu setzen, führt zuArgumentOutOfRangeException.

## Beispiele

Zeigt, wie man Farbe, Farbton und Schattierung für das Design einstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Siehe auch

* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
