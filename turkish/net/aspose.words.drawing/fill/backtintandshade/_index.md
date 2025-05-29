---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: .NET için Aspose.Words
description: Arka plan renginizi zahmetsizce açmak veya koyulaştırmak için BackTintAndShade özelliğini ayarlayın; böylece tasarımınızın görsel çekiciliğini ve kullanıcı deneyimini geliştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Arka plan rengini açan veya koyulaştıran bir double değeri alır veya ayarlar.

```csharp
public double BackTintAndShade { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bu özelliği -1'den küçük veya 1'den büyük bir değere ayarlarsanız fırlatın. |

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişmektedir.

Sıfır (0) nötrdür.

## Örnekler

Ön plan/arka plan şekil renginin tema renginin nasıl ayarlanacağını gösterir.

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
