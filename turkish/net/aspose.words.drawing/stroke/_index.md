---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: .NET için Aspose.Words
description: Şekillerinizi özelleştirilebilir vuruşlarla geliştirmek ve belgelerinize profesyonel bir hava katmak için Aspose.Words.Drawing.Stroke sınıfını keşfedin.
type: docs
weight: 1720
url: /tr/net/aspose.words.drawing/stroke/
---
## Stroke class

Bir şekil için bir kontur tanımlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Şekillerle Çalışma](https://docs.aspose.com/words/net/working-with-shapes/) belgeleme makalesi.

```csharp
public class Stroke
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Konturun arka plan rengini alır veya ayarlar. |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | Kontur arka plan rengini temsil eden bir ThemeColor nesnesi alır veya ayarlar. |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | Vuruş arka plan rengini açan veya koyulaştıran bir çift değer alır veya ayarlar. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | Herhangi bir değiştirici kullanmadan vuruşun temel ön plan rengini alır. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Bir vuruşun rengini tanımlar. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Bir vuruş için ikinci bir renk tanımlar. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Bir vuruş için nokta ve çizgi desenini belirtir. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Bir vuruşun sonu için ok ucu uzunluğunu tanımlar. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Bir vuruşun sonu için ok ucunu tanımlar. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Bir vuruşun sonu için ok ucu genişliğini tanımlar. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Bir vuruşun sonu için kapak stilini tanımlar. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | için doldurma biçimlendirmesini alır`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Konturun ön plan rengini alır veya ayarlar. |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | Vuruş ön plan rengini temsil eden bir ThemeColor nesnesi alır veya ayarlar. |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | Vuruş ön plan rengini açan veya koyulaştıran bir çift değer alır veya ayarlar. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Bir kontur görüntüsü veya desen dolgusu için görüntüyü tanımlar. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Bir poligonun birleştirme stilini tanımlar. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Konturun çizgi stilini tanımlar. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Yolun çizilip çizilmeyeceğini tanımlar. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Bir vuruşun şeffaflık miktarını tanımlar. Geçerli aralık 0 ile 1 arasındadır. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Bir vuruşun başlangıcı için ok ucu uzunluğunu tanımlar. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Bir vuruşun başlangıcı için ok ucunu tanımlar. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Bir vuruşun başlangıcı için ok ucu genişliğini tanımlar. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Darbenin şeffaflık derecesini temsil eden 0,0 (opak) ile 1,0 (temiz) arasında bir değer alır veya ayarlar |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Vuruşun görünür olup olmadığını belirten bir bayrak alır veya ayarlar. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Bir şeklin yolunu noktalar halinde çizen fırça kalınlığını tanımlar. |

## Notlar

Kullanın[`Stroke`](../shape/stroke/)Bir şeklin kontur özelliklerine erişmek için özellik. Örnekleri oluşturmazsınız`Stroke` sınıfa doğrudan.

## Örnekler

Vuruş özelliklerinin nasıl değiştiğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Dikdörtgen gibi temel şekillerin iki görünür kısmı vardır.
// 1 - Şeklin dış hatları içindeki alana uygulanan dolgu:
shape.Fill.ForeColor = Color.White;

// 2 - Şeklin ana hatlarını belirleyen çizgi:
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
