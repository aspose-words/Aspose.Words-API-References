---
title: ParagraphFormat.Borders
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft eine Sammlung von Rändern des Absatzes ab.
type: docs
weight: 60
url: /de/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Ruft eine Sammlung von Rändern des Absatzes ab.

```csharp
public BorderCollection Borders { get; }
```

### Beispiele

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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


