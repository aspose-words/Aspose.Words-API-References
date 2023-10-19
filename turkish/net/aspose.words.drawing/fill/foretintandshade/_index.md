---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words for .NET
description: Fill ForeTintAndShade mülk. Ön plan rengini açan veya koyulaştıran double değerini alır veya ayarlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Ön plan rengini açan veya koyulaştıran double değerini alır veya ayarlar.

```csharp
public double ForeTintAndShade { get; set; }
```

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ila 1 (en açık) aralığındadır. Sıfır (0) nötrdür. Bu özelliği -1'den küçük veya 1 'den büyük bir değere ayarlamaya çalışmak şu sonuçlarla sonuçlanır:ArgumentOutOfRangeException.

## Örnekler

Açıklaştırma ve koyulaştırma ön plan yazı tipi renginin nasıl yönetileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
