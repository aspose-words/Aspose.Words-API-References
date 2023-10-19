---
title: Border.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words for .NET
description: Border ThemeColor mülk. Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır veya ayarlar C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır veya ayarlar.

```csharp
public ThemeColor ThemeColor { get; set; }
```

## Örnekler

Üst kenarlığı olan bir paragrafın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor'ı yalnızca LineWidth veya LineStyle ayarlandığında ayarlayın.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Ayrıca bakınız

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
