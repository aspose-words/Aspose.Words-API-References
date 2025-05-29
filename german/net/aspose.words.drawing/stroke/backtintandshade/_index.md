---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words für .NET
description: Passen Sie die Hintergrundfarbe Ihres Strichs mühelos mit Stroke BackTintAndShade an. Steuern Sie Helligkeit und Dunkelheit für ein perfektes Design-Finish.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der die Hintergrundfarbe des Strichs aufhellt oder abdunkelt.

```csharp
public double BackTintAndShade { get; set; }
```

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (dunkelster Wert) bis 1 (hellster Wert). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 zu setzen, führt zuArgumentOutOfRangeException.

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

* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
