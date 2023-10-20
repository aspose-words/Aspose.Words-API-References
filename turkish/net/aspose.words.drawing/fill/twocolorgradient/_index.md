---
title: Fill.TwoColorGradient
linktitle: TwoColorGradient
articleTitle: TwoColorGradient
second_title: Aspose.Words for .NET
description: Fill TwoColorGradient yöntem. Belirtilen dolguyu iki renkli degradeye ayarlar C#'da.
type: docs
weight: 260
url: /tr/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/)*) {#twocolorgradient}

Belirtilen dolguyu iki renkli degradeye ayarlar.

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| style | GradientStyle | Degrade stili[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | Degrade varyantı[`GradientVariant`](../../gradientvariant/) |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)

---

## TwoColorGradient(*Color, Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/)*) {#twocolorgradient_1}

Belirtilen dolguyu iki renkli degradeye ayarlar.

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| color1 | Color | Degradeyi oluşturan ilk renk. |
| color2 | Color | Degradeyi oluşturmak için ikinci renk. |
| style | GradientStyle | Degrade stili[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | Degrade varyantı[`GradientVariant`](../../gradientvariant/) |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
