---
title: Stroke.StartArrowWidth
linktitle: StartArrowWidth
articleTitle: StartArrowWidth
second_title: .NET için Aspose.Words
description: Vuruşlarınızın ok ucu genişliğini özelleştirmek, tasarımınızın hassasiyetini ve görsel çekiciliğini artırmak için Stroke StartArrowWidth özelliğini keşfedin.
type: docs
weight: 230
url: /tr/net/aspose.words.drawing/stroke/startarrowwidth/
---
## Stroke.StartArrowWidth property

Bir vuruşun başlangıcı için ok ucu genişliğini tanımlar.

```csharp
public ArrowWidth StartArrowWidth { get; set; }
```

## Notlar

Varsayılan değer:Medium.

## Örnekler

Çeşitli şekiller yaratmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda belgelerimize ekleyebileceğimiz şekillerin dört örneği bulunmaktadır.
// 1 - Noktalı, yatay, yarı saydam kırmızı çizgi
// sol ucunda bir ok ve sağ ucunda bir elmas bulunan:
Shape arrow = new Shape(doc, ShapeType.Line);
arrow.Width = 200;
arrow.Stroke.Color = Color.Red;
arrow.Stroke.StartArrowType = ArrowType.Arrow;
arrow.Stroke.StartArrowLength = ArrowLength.Long;
arrow.Stroke.StartArrowWidth = ArrowWidth.Wide;
arrow.Stroke.EndArrowType = ArrowType.Diamond;
arrow.Stroke.EndArrowLength = ArrowLength.Long;
arrow.Stroke.EndArrowWidth = ArrowWidth.Wide;
arrow.Stroke.DashStyle = DashStyle.Dash;
arrow.Stroke.Opacity = 0.5;

Assert.AreEqual(JoinStyle.Miter, arrow.Stroke.JoinStyle);

builder.InsertNode(arrow);

// 2 - Uçları yuvarlatılmış kalın siyah çapraz çizgi:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Yeşil dolgulu ok:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - Aspose logosuyla doldurulmuş, ters yöne bakan ok:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Okumuzun yönünü çevirdiğimizde, okun içerdiği görüntüyü de çevirmiş oluyoruz.
    // Şekli görüntülemeden önce bunu iptal etmek için görüntüyü diğer yöne çevirin.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Ayrıca bakınız

* enum [ArrowWidth](../../arrowwidth/)
* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
