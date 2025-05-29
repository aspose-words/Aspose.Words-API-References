---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: .NET için Aspose.Words
description: Stroke ForeTintAndShade özelliğini ayarlayarak vuruşunuzun ön plan rengini kolayca açın veya koyulaştırın ve görsel etkiyi artırın.
type: docs
weight: 150
url: /tr/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Vuruş ön plan rengini açan veya koyulaştıran bir çift değer alır veya ayarlar.

```csharp
public double ForeTintAndShade { get; set; }
```

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişir. Sıfır (0) nötrdür. Bu özelliği -1'den küçük veya 1 'den büyük bir değere ayarlamaya çalışmak şu sonucu verir:ArgumentOutOfRangeException.

## Örnekler

Ön tema renginin, tonunun ve gölgesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Ayrıca bakınız

* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
