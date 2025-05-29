---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: .NET için Aspose.Words
description: Gelişmiş dolgu biçimlendirme seçenekleri için Aspose.Words.Drawing.Fill sınıfını keşfedin, belge tasarımınızı ve görsel çekiciliğinizi zahmetsizce geliştirin.
type: docs
weight: 1270
url: /tr/net/aspose.words.drawing/fill/
---
## Fill class

Bir nesne için dolgu biçimlendirmesini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafik Öğelerle Çalışma](https://docs.aspose.com/words/net/working-with-graphic-elements/) belgeleme makalesi.

```csharp
public class Fill
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Dolgu için arka plan rengini temsil eden bir Renk nesnesi alır veya ayarlar. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Dolgu için arka plan rengini temsil eden bir ThemeColor nesnesi alır veya ayarlar. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Arka plan rengini açan veya koyulaştıran bir double değeri alır veya ayarlar. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } | Herhangi bir değiştirici olmadan fill için temel ön plan rengini temsil eden bir Renk nesnesi alır. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Dolgu için ön plan rengini temsil eden bir Renk nesnesi alır veya ayarlar. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Bir dolgu türü alır. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Dolgu için ön plan rengini temsil eden bir Renk nesnesi alır veya ayarlar. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Dolgu için ön plan rengini temsil eden bir ThemeColor nesnesi alır veya ayarlar. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Ön plan rengini açan veya koyulaştıran bir çift değer alır veya ayarlar. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Degrade dolgusunun açısını alır veya ayarlar. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Bir koleksiyon alır[`GradientStop`](../gradientstop/) dolgu için nesneler. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Gradyan stilini alır[`GradientStyle`](../gradientstyle/) dolgu için. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Gradyan varyantını alır[`GradientVariant`](../gradientvariant/) dolgu için. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Dolgu dokusunun veya deseninin ham baytlarını alır. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Belirtilen dolgunun opaklık derecesini 0,0 (temiz) ile 1,0 (opak) arasında bir değer olarak alır veya ayarlar. |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Bir tane alır[`PatternType`](../patterntype/) dolgu için. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Bir tane alır[`PresetTexture`](../presettexture/) dolgu için. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Dolgunun belirtilen nesneyle birlikte dönüp dönmeyeceğini alır veya ayarlar. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Döşeme doku dolgusu için hizalamayı alır veya ayarlar. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Belirtilen dolgunun şeffaflık derecesini 0,0 (opak) ile 1,0 (temiz) arasında bir değer olarak alır veya ayarlar. |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Değeri alır veya ayarlar`doğru` bu örneğe uygulanan biçimlendirme görünürse. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Belirtilen dolguyu tek renkli bir degradeye ayarlar. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Belirtilen dolguyu belirtilen rengi kullanarak tek renkli bir degradeye ayarlar. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | Belirtilen dolguyu bir desene ayarlar. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | Belirtilen dolguyu bir desene ayarlar. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | Dolguyu önceden ayarlanmış bir dokuya ayarlar. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | Dolgu türünü tek görüntüye değiştirir. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | Dolgu türünü tek görüntüye değiştirir. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | Dolgu türünü tek görüntüye değiştirir. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Dolguyu tekdüze bir renge ayarlar. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | Dolguyu belirtilen tekdüze bir renge ayarlar. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Belirtilen dolguyu iki renkli bir degradeye ayarlar. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Belirtilen dolguyu iki renkli bir degradeye ayarlar. |

## Notlar

Kullanın[`Fill`](../shapebase/fill/) veya[`Fill`](../../aspose.words/font/fill/) Bir nesnenin dolgu özelliklerine erişmek için özellik. Örnekleri oluşturmazsınız`Fill` sınıfa doğrudan.

## Örnekler

Bir şeklin düz bir renkle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Biraz metin yazın ve ardından onu yüzen bir şekille örtün.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Şeklin dış hatlarının rengini ayarlamak için "StrokeColor" özelliğini kullanın.
shape.StrokeColor = Color.CadetBlue;

// Şeklin iç alanının rengini ayarlamak için "FillColor" özelliğini kullanın.
shape.FillColor = Color.LightBlue;

// "Opaklık" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak, 0 ise görünmez anlamına gelir.
// Şeklin dolgusu varsayılan olarak tamamen opak olduğundan, şeklin üstündeki metni göremeyiz.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Şeklin dolgu renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
