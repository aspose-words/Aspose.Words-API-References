---
title: Enum GradientVariant
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.GradientVariant Sıralama. Degrade dolgusu için varyantı belirtir.
type: docs
weight: 880
url: /tr/net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

Degrade dolgusu için varyantı belirtir.

```csharp
public enum GradientVariant
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Gradyan değişkeni 'Yok'. |
| Variant1 | `1` | Gradyan değişkeni 1. |
| Variant2 | `2` | Gradyan değişkeni 2. |
| Variant3 | `3` | Gradyan değişkeni 3. |
| Variant4 | `4` | Gradyan değişkeni 4. |

### Notlar

Word'deki Dolgu Efektleri iletişim kutusundaki Degrade sekmesindeki dört varyanta karşılık gelir.

### Örnekler

Bir şeklin degradelerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// ForeColor degrade dolgusu ile şekle Tek renkli degrade dolgu uygulayın.
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
// "GradientStyle.FromCorner/GradientStyle.FromCenter" için "GradientAngle" değiştirildiğini unutmayın
// gradyan dolgu herhangi bir efekt almaz, sadece lineer gradyan için çalışır.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// "GradientStyle" almak istiyorsanız DML kullanarak şekli tanımlamak için uyumluluk seçeneğini kullanın,
// Belge kaydedildikten sonra "GradientVariant" ve "GradientAngle" özellikleri.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


