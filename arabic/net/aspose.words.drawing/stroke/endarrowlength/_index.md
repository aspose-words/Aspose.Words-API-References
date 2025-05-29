---
title: Stroke.EndArrowLength
linktitle: EndArrowLength
articleTitle: EndArrowLength
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Stroke EndArrowLength لتخصيص تصميمك بأطوال دقيقة لرؤوس الأسهم، مما يعزز الوضوح البصري والأناقة.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/stroke/endarrowlength/
---
## Stroke.EndArrowLength property

يحدد طول رأس السهم لنهاية الخط.

```csharp
public ArrowLength EndArrowLength { get; set; }
```

## ملاحظات

القيمة الافتراضية هيMedium.

## أمثلة

يظهر كيفية إنشاء مجموعة متنوعة من الأشكال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي أربعة أمثلة للأشكال التي يمكننا إدراجها في مستنداتنا.
// 1 - خط أحمر منقط، أفقي، نصف شفاف
// مع سهم على الطرف الأيسر ومعين على الطرف الأيمن:
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

// 2 - خط قطري أسود سميك ذو أطراف مستديرة:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - سهم مع تعبئة خضراء:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - سهم ذو اتجاه مقلوب مملوء بشعار Aspose:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // عندما نقوم بتغيير اتجاه السهم، فإننا نقوم أيضًا بتغيير الصورة التي يحتويها السهم.
    // قم بقلب الصورة إلى الاتجاه الآخر لإلغاء هذا قبل عرض الشكل.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### أنظر أيضا

* enum [ArrowLength](../../arrowlength/)
* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
