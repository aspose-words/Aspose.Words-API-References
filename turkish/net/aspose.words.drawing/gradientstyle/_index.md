---
title: GradientStyle Enum
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.GradientStyle Sıralama. Degrade dolgunun stilini belirtir C#'da.
type: docs
weight: 1000
url: /tr/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

Degrade dolgunun stilini belirtir.

```csharp
public enum GradientStyle
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `-1` | Degrade yok. |
| Horizontal | `1` | Bir nesne boyunca yatay olarak uzanan degrade. |
| Vertical | `2` | Bir nesneden aşağıya dikey olarak uzanan degrade. |
| DiagonalUp | `3` | Alt köşeden karşı köşeye doğru hareket eden çapraz degrade. |
| DiagonalDown | `4` | Üst köşeden karşı köşeye doğru hareket eden çapraz degrade. |
| FromCorner | `5` | Bir köşeden diğer üç köşeye uzanan degrade. |
| FromCenter | `6` | Merkezden köşelere doğru uzanan degrade. |

## Örnekler

Bir şeklin degradelerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Degrade dolgunun ForeColor'unu kullanarak şekle Tek renkli degrade dolgu uygulayın.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Şekle iki renkli degrade dolgu uygulayın.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Degrade dolgunun BackColor'ını değiştirin.
shape.Fill.BackColor = Color.Yellow;
// "GradientStyle.FromCorner/GradientStyle.FromCenter" için "GradientAngle"ın değiştiğini unutmayın
// degrade dolgusu herhangi bir etki yaratmaz, yalnızca doğrusal degrade için çalışır.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// "GradientStyle" elde etmek istiyorsanız şekli DML kullanarak tanımlamak için uyumluluk seçeneğini kullanın,
// Belge kaydedildikten sonra "GradientVariant" ve "GradientAngle" özellikleri.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
