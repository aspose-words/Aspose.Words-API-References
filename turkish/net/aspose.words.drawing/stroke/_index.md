---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Stroke sınıf. Bir şeklin konturunu tanımlar C#'da.
type: docs
weight: 1310
url: /tr/net/aspose.words.drawing/stroke/
---
## Stroke class

Bir şeklin konturunu tanımlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Şekillerle Çalışmak](https://docs.aspose.com/words/net/working-with-shapes/) dokümantasyon makalesi.

```csharp
public class Stroke
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Konturun arka plan rengini alır veya ayarlar. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Konturun rengini tanımlar. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Kontur için ikinci rengi tanımlar. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Kontur için nokta ve çizgi desenini belirtir. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Kontur sonu için ok ucu uzunluğunu tanımlar. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Konturun sonu için ok ucunu tanımlar. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Konturun sonu için ok ucu genişliğini tanımlar. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Konturun sonu için başlık stilini tanımlar. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | Dolgu formatını alır`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Konturun ön plan rengini alır veya ayarlar. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Kontur görüntüsü veya desen dolgusu için görüntüyü tanımlar. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Sürekli çizginin birleştirme stilini tanımlar. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Konturun çizgi stilini tanımlar. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Yolun vuruşlu olup olmayacağını tanımlar. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Konturun şeffaflık miktarını tanımlar. Geçerli aralık 0 ila 1. arasındadır |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Bir vuruşun başlangıcı için ok ucu uzunluğunu tanımlar. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Konturun başlangıcı için ok ucunu tanımlar. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Konturun başlangıcı için ok ucu genişliğini tanımlar. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Konturun şeffaflık derecesini temsil eden 0,0 (opak) ile 1,0 (şeffaf) arasında bir değer alır veya ayarlar. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Konturun görünür olup olmadığını belirten bir bayrak alır veya ayarlar. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Bir şeklin yolunu nokta olarak konturlayan fırça kalınlığını tanımlar. |

## Notlar

Kullan[`Stroke`](../shape/stroke/) bir şeklin kontur özelliklerine erişim özelliği. `Stroke` doğrudan sınıf.

## Örnekler

Kontur özelliklerinin nasıl değiştirildiğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Dikdörtgen gibi temel şekillerin iki görünür kısmı vardır.
// 1 - Şeklin ana hatları içindeki alana uygulanan dolgu:
shape.Fill.ForeColor = Color.White;

// 2 - Şeklin ana hatlarını işaretleyen kontur:
// Bu şeklin konturunun çeşitli özelliklerini değiştirin.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
