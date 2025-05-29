---
title: ParagraphFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: .NET için Aspose.Words
description: Paragraf kenarlıklarınızı kolayca yönetmek ve özelleştirmek, belge estetiğini ve okunabilirliğini artırmak için ParagraphFormat Borders özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Paragrafın kenarlıklarının koleksiyonunu alır.

```csharp
public BorderCollection Borders { get; }
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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
