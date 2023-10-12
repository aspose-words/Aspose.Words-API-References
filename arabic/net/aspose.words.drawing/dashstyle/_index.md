---
title: Enum DashStyle
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.DashStyle تعداد. نمط الخط المتقطع.
type: docs
weight: 930
url: /ar/net/aspose.words.drawing/dashstyle/
---
## DashStyle enumeration

نمط الخط المتقطع.

```csharp
public enum DashStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Solid | `0` | قلم مصمت (مستمر). |
| ShortDash | `1` | نمط شرطة النظام. |
| ShortDot | `2` | نمط شرطة النظام. |
| ShortDashDot | `3` | نمط شرطة النظام. |
| ShortDashDotDot | `4` | نمط شرطة النظام. |
| Dot | `5` | نمط النقطة المربعة. |
| Dash | `6` | نمط الشرطة. |
| LongDash | `7` | نمط الشرطة الطويلة. |
| DashDot | `8` | شرطة قصيرة. |
| LongDashDot | `9` | شرطة طويلة شرطة قصيرة. |
| LongDashDotDot | `10` | شرطة طويلة شرطة قصيرة شرطة قصيرة. |
| Default | `0` | نفسSolid . |

### أمثلة

يظهر لإنشاء مجموعة متنوعة من الأشكال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي أربعة أمثلة للأشكال التي يمكننا إدراجها في مستنداتنا.
// 1 - خط أحمر منقط، أفقي، نصف شفاف
// مع وجود سهم على الطرف الأيسر وماسة على الطرف الأيمن:
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

// 2 - خط قطري سميك أسود ذو أطراف مستديرة:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - سهم ذو تعبئة خضراء:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - سهم ذو اتجاه معكوس مملوء بشعار Aspose:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // عندما نقلب اتجاه سهمنا، فإننا نقلب أيضًا الصورة التي يحتوي عليها السهم.
    // اقلب الصورة في الاتجاه الآخر لإلغاء ذلك قبل الحصول على الشكل لعرضه.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### أنظر أيضا

* property [DashStyle](../stroke/dashstyle/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


