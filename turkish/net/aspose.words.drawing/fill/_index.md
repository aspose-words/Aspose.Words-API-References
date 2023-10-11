---
title: Class Fill
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Fill sınıf. Bir nesnenin dolgu biçimlendirmesini temsil eder.
type: docs
weight: 950
url: /tr/net/aspose.words.drawing/fill/
---
## Fill class

Bir nesnenin dolgu biçimlendirmesini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafik Öğeleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-graphic-elements/) dokümantasyon makalesi.

```csharp
public class Fill
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Dolgunun arka plan rengini temsil eden bir Color nesnesini alır veya ayarlar. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Dolgunun arka plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Arka plan rengini açan veya koyulaştıran double değerini alır veya ayarlar. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } |  |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Dolgunun ön plan rengini temsil eden bir Color nesnesini alır veya ayarlar. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Bir dolgu türü alır. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Dolgunun ön plan rengini temsil eden bir Color nesnesini alır veya ayarlar. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Dolgunun ön plan rengini temsil eden ThemeColor nesnesini alır veya ayarlar. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Ön plan rengini açan veya koyulaştıran double değerini alır veya ayarlar. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Degrade dolgunun açısını alır veya ayarlar. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Şunlardan oluşan bir koleksiyon alır:[`GradientStop`](../gradientstop/) dolgu için nesneler. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Degrade stilini alır[`GradientStyle`](../gradientstyle/) dolgu için. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Degrade değişkenini alır[`GradientVariant`](../gradientvariant/) dolgu için. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Dolgu dokusunun veya deseninin ham baytlarını alır. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Belirtilen dolgunun opaklık derecesini 0,0 (açık) ile 1,0 (opak) arasında bir değer olarak alır veya ayarlar. |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Bir alır[`PatternType`](../patterntype/) dolgu için. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Bir alır[`PresetTexture`](../presettexture/) dolgu için. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Dolgunun belirtilen nesneyle birlikte dönüp dönmeyeceğini alır veya ayarlar. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Döşeme dokusu dolgusunun hizalamasını alır veya ayarlar. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Belirtilen dolgunun şeffaflık derecesini 0,0 (opak) ile 1,0 (şeffaf) arasında bir değer olarak alır veya ayarlar. |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Şu değeri alır veya ayarlar:`doğru` bu örneğe uygulanan biçimlendirme görünüyorsa. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | Belirtilen dolguyu tek renkli bir degradeye ayarlar. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | Belirtilen rengi kullanarak, belirtilen dolguyu tek renkli bir degradeye ayarlar. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | Belirtilen dolguyu bir desene ayarlar. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | Belirtilen dolguyu bir desene ayarlar. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | Dolguyu önceden ayarlanmış bir dokuya ayarlar. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | Doldurma türünü tek görüntü olarak değiştirir. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | Doldurma türünü tek görüntü olarak değiştirir. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | Doldurma türünü tek görüntü olarak değiştirir. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Dolguyu tek tip bir renge ayarlar. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | Dolguyu belirtilen tekdüze renge ayarlar. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | Belirtilen dolguyu iki renkli degradeye ayarlar. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | Belirtilen dolguyu iki renkli degradeye ayarlar. |

### Notlar

Kullan[`Fill`](../shapebase/fill/) veya[`Fill`](../../aspose.words/font/fill/) bir nesnenin dolgu özelliklerine erişim özelliği. Örneklerini oluşturmazsınız`Fill` doğrudan sınıf.

### Örnekler

Bir şeklin düz renkle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir miktar metin yazın ve ardından onu kayan bir şekille kaplayın.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Şeklin anahattının rengini ayarlamak için "StrokeColor" özelliğini kullanın.
shape.StrokeColor = Color.CadetBlue;

// Şeklin iç alanının rengini ayarlamak için "FillColor" özelliğini kullanın.
shape.FillColor = Color.LightBlue;

// "Opaklık" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak ve 0 görünmez olacak şekilde.
// Şekil dolgusu varsayılan olarak tamamen opaktır, dolayısıyla bu şeklin üstünde olduğu metni göremiyoruz.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Şekil dolgu renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


