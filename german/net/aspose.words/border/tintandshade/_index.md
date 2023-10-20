---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words für .NET
description: Border TintAndShade eigendom. Ruft einen DoubleWert ab oder legt ihn fest der eine Farbe heller oder dunkler macht in C#.
type: docs
weight: 80
url: /de/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Ruft einen Double-Wert ab oder legt ihn fest, der eine Farbe heller oder dunkler macht.

```csharp
public double TintAndShade { get; set; }
```

## Bemerkungen

Die zulässigen Werte für diese Eigenschaft liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder mehr als 1 festzulegen, führt zuArgumentOutOfRangeException.

Das Festlegen dieser Eigenschaft für ein Rahmenobjekt mit Nicht-Theme-Farben führt zuInvalidOperationException.

## Beispiele

Zeigt, wie ein Absatz mit einem oberen Rand eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor nur festlegen, wenn LineWidth oder LineStyle festgelegt ist.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Siehe auch

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
