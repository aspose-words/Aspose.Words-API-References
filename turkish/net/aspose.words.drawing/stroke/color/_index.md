---
title: Stroke.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: Stroke Color mülk. Konturun rengini tanımlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/stroke/color/
---
## Stroke.Color property

Konturun rengini tanımlar.

```csharp
public Color Color { get; set; }
```

## Notlar

Bir için varsayılan değer[`Shape`](../../shape/) is Black.

## Örnekler

Çeşitli şekiller oluşturmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda belgelerimize ekleyebileceğimiz dört şekil örneği verilmiştir.
// 1 - Noktalı, yatay, yarı şeffaf kırmızı çizgi
// sol uçta bir ok ve sağ uçta bir baklava işaretiyle:
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

// 2 - Yuvarlak uçlu kalın siyah çapraz çizgi:
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

// 4 - Aspose logosuyla dolu ters çevrilmiş yönlendirmeli ok:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Okumuzun yönünü çevirdiğimizde okun içerdiği görüntüyü de çevirmiş oluyoruz.
    // Gösterilecek şekli almadan önce bunu iptal etmek için görüntüyü diğer yöne çevirin.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Ayrıca bakınız

* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
