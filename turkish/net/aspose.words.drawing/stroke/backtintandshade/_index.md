---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: .NET için Aspose.Words
description: Stroke BackTintAndShade ile vuruş arka plan renginizi zahmetsizce ayarlayın. Mükemmel bir tasarım sonucu için açıklığı ve koyuluğu kontrol edin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Vuruş arka plan rengini açan veya koyulaştıran bir çift değer alır veya ayarlar.

```csharp
public double BackTintAndShade { get; set; }
```

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişir. Sıfır (0) nötrdür. Bu özelliği -1'den küçük veya 1 'den büyük bir değere ayarlamaya çalışmak şu sonucu verir:ArgumentOutOfRangeException.

## Örnekler

Tema renginin, tonunun ve gölgesinin nasıl geri ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Ayrıca bakınız

* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
