---
title: Border.TintAndShade
second_title: Aspose.Words for .NET API Referansı
description: Border mülk. Bir rengi açan veya koyulaştıran double değerini alır veya ayarlar.
type: docs
weight: 80
url: /tr/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Bir rengi açan veya koyulaştıran double değerini alır veya ayarlar.

```csharp
public double TintAndShade { get; set; }
```

### Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ila 1 (en açık) aralığındadır. Sıfır (0) nötrdür. Bu özelliği -1'den küçük veya 1 'den büyük bir değere ayarlamaya çalışmak şu sonuçlarla sonuçlanır:ArgumentOutOfRangeException.

Bu özelliğin Border nesnesi için tema dışı colours ile ayarlanması şu sonucu doğurur:InvalidOperationException.

### Örnekler

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
* ad alanı [Aspose.Words](../../border/)
* toplantı [Aspose.Words](../../../)


