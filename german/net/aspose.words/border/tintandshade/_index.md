---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words für .NET
description: Entdecken Sie Border TintAndShade und passen Sie die Farbhelligkeit mühelos mit einem einfachen Doppelwert an, um beeindruckende Designverbesserungen zu erzielen. Perfekt für Ihre kreativen Projekte!
type: docs
weight: 80
url: /de/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der eine Farbe aufhellt oder abdunkelt.

```csharp
public double TintAndShade { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn Sie versuchen, diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 festzulegen. |
| InvalidOperationException | Wird ausgelöst, wenn diese Eigenschaft für ein Rahmenobjekt mit nicht zum Design gehörenden Farben festgelegt wird. |

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (dunkelster Wert) bis 1 (hellster Wert). Null (0) ist neutral.

## Beispiele

Zeigt, wie ein Absatz mit einem oberen Rand eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor nur festlegen, wenn LineWidth oder LineStyle festgelegt sind.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Siehe auch

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
