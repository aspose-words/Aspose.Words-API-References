---
title: Border.ThemeColor
second_title: Aspose.Words für .NET-API-Referenz
description: Border eigendom. Ruft die Designfarbe im angewendeten Farbschema ab das diesem BorderObjekt zugeordnet ist oder legt diese fest.
type: docs
weight: 70
url: /de/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Ruft die Designfarbe im angewendeten Farbschema ab, das diesem Border-Objekt zugeordnet ist, oder legt diese fest.

```csharp
public ThemeColor ThemeColor { get; set; }
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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* namensraum [Aspose.Words](../../border/)
* Montage [Aspose.Words](../../../)


