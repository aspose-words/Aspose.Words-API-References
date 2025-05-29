---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: .NET için Aspose.Words
description: Ön plan renginizi kolayca açmak veya koyulaştırmak için ForeTintAndShade özelliğini ayarlayın, tasarımınızı hassasiyet ve yaratıcılıkla geliştirin.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Ön plan rengini açan veya koyulaştıran bir çift değer alır veya ayarlar.

```csharp
public double ForeTintAndShade { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bu özelliği -1'den küçük veya 1'den büyük bir değere ayarlarsanız fırlatın. |

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişmektedir.

Sıfır (0) nötrdür.

## Örnekler

Ön plandaki yazı renginin nasıl açılıp koyulaştırılacağını gösterir.

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
