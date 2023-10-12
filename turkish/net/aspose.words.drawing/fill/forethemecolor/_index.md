---
title: Fill.ForeThemeColor
second_title: Aspose.Words for .NET API Referansı
description: Fill mülk. Dolgunun ön plan rengini temsil eden ThemeColor nesnesini alır veya ayarlar.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Dolgunun ön plan rengini temsil eden ThemeColor nesnesini alır veya ayarlar.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

### Örnekler

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)


