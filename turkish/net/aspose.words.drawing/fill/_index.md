---
title: Class Fill
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Fill sınıf. Bir nesne için dolgu biçimlendirmesini temsil eder.
type: docs
weight: 820
url: /tr/net/aspose.words.drawing/fill/
---
## Fill class

Bir nesne için dolgu biçimlendirmesini temsil eder.

```csharp
public class Fill
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Dolgu için arka plan rengini temsil eden bir Color nesnesi alır veya ayarlar. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Bir dolgu türü alır. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Dolgu için ön plan rengini temsil eden bir Color nesnesi alır veya ayarlar. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Degrade dolgunun açısını alır veya ayarlar. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Bir koleksiyon alır[`GradientStop`](../gradientstop/) dolgu için nesneler. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Degrade stilini alır[`GradientStyle`](../gradientstyle/) dolgu için. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Degrade değişkenini alır[`GradientVariant`](../gradientvariant/) dolgu için. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Dolgu dokusunun veya deseninin ham baytlarını alır. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Belirtilen dolgunun opaklık derecesini 0.0 (net) ile 1.0 (opak) arasında bir değer olarak alır veya ayarlar. |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | [`PatternType`](../patterntype/) dolgu için. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | [`PresetTexture`](../presettexture/) dolgu için. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Dolgunun belirtilen nesneyle birlikte dönüp dönmediğini alır veya ayarlar. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Döşeme dokusu dolgusu için hizalamayı alır veya ayarlar. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Belirtilen dolgunun şeffaflık derecesini 0.0 (opak) ile 1.0 (net) arasında bir değer olarak alır veya ayarlar. |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Şu değeri alır veya ayarlar:`doğru` bu örneğe uygulanan biçimlendirme görünürse. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | Belirtilen dolguyu tek renkli bir degradeye ayarlar. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | Belirtilen dolguyu, belirtilen rengi kullanarak tek renkli bir degradeye ayarlar. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | Belirtilen dolguyu bir kalıba ayarlar. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | Belirtilen dolguyu bir kalıba ayarlar. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | Dolguyu önceden ayarlanmış bir dokuya ayarlar. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | Doldurma türünü tek görüntü olarak değiştirir. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | Doldurma türünü tek görüntü olarak değiştirir. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | Doldurma türünü tek görüntü olarak değiştirir. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Dolguyu tek tip bir renge ayarlar. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | Dolguyu belirtilen tek tip renge ayarlar. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | Belirtilen dolguyu iki renkli bir degradeye ayarlar. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | Belirtilen dolguyu iki renkli bir degradeye ayarlar. |

### Notlar

Kullan[`Fill`](../shapebase/fill/) veya[`Fill`](../../aspose.words/font/fill/) bir nesnenin dolgu özelliklerine erişme özelliği. `Fill` doğrudan sınıf.

### Örnekler

Bir şeklin düz bir renkle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir metin yazın ve ardından kayan bir şekille kaplayın.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Şeklin anahattının rengini ayarlamak için "StrokeColor" özelliğini kullanın.
shape.StrokeColor = Color.CadetBlue;

// Şeklin iç alanının rengini ayarlamak için "FillColor" özelliğini kullanın.
shape.FillColor = Color.LightBlue;

// "Opacity" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak ve 0 görünmez olmak üzere.
// Şekil dolgusu varsayılan olarak tamamen opaktır, bu nedenle bu şeklin üzerinde olduğu metni göremeyiz.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Altındaki metni görebilmemiz için şekil dolgu renginin opaklığını daha düşük bir değere ayarlayın.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


