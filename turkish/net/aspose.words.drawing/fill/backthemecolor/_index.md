---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: .NET için Aspose.Words
description: BackThemeColor özelliğiyle tasarımınızı özelleştirin. Arka plan dolgunuzu geliştirmek ve kullanıcı deneyiminizi yükseltmek için kolayca bir ThemeColor nesnesi ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

Dolgu için arka plan rengini temsil eden bir ThemeColor nesnesi alır veya ayarlar.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
