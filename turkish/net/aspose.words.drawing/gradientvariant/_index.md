---
title: GradientVariant Enum
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: .NET için Aspose.Words
description: Özelleştirilebilir degrade dolgular için Aspose.Words.Drawing.GradientVariant enum'unu keşfedin ve belge tasarımlarınızı canlı stillerle geliştirin.
type: docs
weight: 1340
url: /tr/net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

Bir degrade dolgusu için varyantı belirtir.

```csharp
public enum GradientVariant
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Gradyan değişkeni 'Hiçbiri'. |
| Variant1 | `1` | Gradyan varyantı 1. |
| Variant2 | `2` | Gradyan varyantı 2. |
| Variant3 | `3` | Gradyan varyantı 3. |
| Variant4 | `4` | Gradyan varyantı 4. |

## Notlar

Word'deki Dolgu Efektleri iletişim kutusundaki Degrade sekmesindeki dört çeşide karşılık gelir.

## Örnekler

Bir şeklin degradelerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// ForeColor'ı degrade dolgu olarak kullanarak şekle tek renkli degrade dolgu uygulayın.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Şekle iki renkli degrade dolgusu uygula.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Degrade dolgusunun BackColor'ını değiştir.
shape.Fill.BackColor = Color.Yellow;
// "GradientStyle.FromCorner/GradientStyle.FromCenter" için "GradientAngle" değişikliklerine dikkat edin
// degrade dolgunun herhangi bir etkisi olmaz, sadece doğrusal degrade için çalışır.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// "GradientStyle" elde etmek istiyorsanız, DML kullanarak şekli tanımlamak için uyumluluk seçeneğini kullanın.
// Belge kaydedildikten sonra "GradientVariant" ve "GradientAngle" özellikleri.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
