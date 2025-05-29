---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: .NET için Aspose.Words
description: Border TintAndShade'i keşfedin, çarpıcı tasarım geliştirmeleri için basit bir çift değerle renk parlaklığını zahmetsizce ayarlayın. Yaratıcı projeleriniz için mükemmel!
type: docs
weight: 80
url: /tr/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Bir rengi açan veya koyulaştıran bir double değeri alır veya ayarlar.

```csharp
public double TintAndShade { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bu özelliği -1'den küçük veya 1'den büyük bir değere ayarlamayı denerseniz fırlatır. |
| InvalidOperationException | Bu özelliğin Border nesnesi için tema renkleri dışında bir renkle ayarlanması durumunda oluşur. |

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişmektedir. Sıfır (0) nötrdür.

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

* class [Border](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
