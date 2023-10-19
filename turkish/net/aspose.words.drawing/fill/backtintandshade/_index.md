---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words for .NET
description: Fill BackTintAndShade mülk. Arka plan rengini açan veya koyulaştıran double değerini alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Arka plan rengini açan veya koyulaştıran double değerini alır veya ayarlar.

```csharp
public double BackTintAndShade { get; set; }
```

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ila 1 (en açık) aralığındadır. Sıfır (0) nötrdür. Bu özelliği -1'den küçük veya 1 'den büyük bir değere ayarlamaya çalışmak şu sonuçlarla sonuçlanır:ArgumentOutOfRangeException.

## Örnekler

Ön plan/arka plan şekli rengi için tema renginin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Not: Yazı tipi dolgusu için "BackThemeColor" ve "BackTintAndShade" kullanmayın.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
