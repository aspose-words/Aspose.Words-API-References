---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.RelativeVerticalSize enum، الذي يحدد حسابات الارتفاع الرأسي للأشكال وإطارات النص، مما يعزز دقة تخطيط المستند.
type: docs
weight: 1610
url: /ar/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

يحدد بشكل نسبي ما يتم حسابه من ارتفاع الشكل أو إطار النص عموديًا.

```csharp
public enum RelativeVerticalSize
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Margin | `0` | يحدد أن الارتفاع يتم حسابه نسبيًا بالنسبة للمسافة بين الهامش العلوي والسفلي. |
| Page | `1` | يحدد أن الارتفاع يتم حسابه نسبيًا لارتفاع الصفحة. |
| TopMargin | `2` | يحدد أن الارتفاع يتم حسابه نسبيًا لحجم منطقة الهامش العلوي. |
| BottomMargin | `3` | يحدد أن الارتفاع يتم حسابه نسبيًا لحجم منطقة الهامش السفلي. |
| InnerMargin | `4` | يحدد أن الارتفاع يتم حسابه نسبيًا إلى حجم منطقة الهامش الداخلي، إلى حجم منطقة الهامش العلوي للصفحات الفردية وإلى حجم منطقة الهامش السفلي للصفحات الزوجية. |
| OuterMargin | `5` | يحدد أن الارتفاع يتم حسابه نسبيًا إلى حجم منطقة الهامش الخارجي، إلى حجم منطقة الهامش السفلي للصفحات الفردية وإلى حجم منطقة الهامش العلوي للصفحات الزوجية. |
| Default | `1` | القيمة الافتراضية هيMargin . |

## أمثلة

يوضح كيفية تعيين الحجم والموضع النسبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إضافة شكل بسيط بالحجم والموضع المطلق.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// قم بتعيين WrapType إلى WrapType.None نظرًا لأن الأشكال المضمنة يتم تحويلها تلقائيًا إلى وحدات مطلقة.
shape.WrapType = WrapType.None;

// التحقق من الحجم الأفقي النسبي وتعيينه.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // تعيين حجم الربط الأفقي إلى الهامش.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // ضبط العرض إلى 50% من عرض الهامش.
    shape.WidthRelative = 50;
}

// التحقق من الحجم الرأسي النسبي وتعيينه.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // تعيين حجم الربط الرأسي إلى الهامش.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // ضبط الارتفاع إلى 30% من ارتفاع الهامش.
    shape.HeightRelative = 30;
}

// التحقق من الموضع الرأسي النسبي وتعيينه.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // تعيين ربط الموضع إلى TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // ضبط الجزء العلوي النسبي إلى 30% من موضع TopMargin.
    shape.TopRelative = 30;
}

// التحقق من الموضع الأفقي النسبي وتعيينه.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // تعيين ربط الموضع إلى RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    //يمكن أن تكون القيمة النسبية للموضع سلبية.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### أنظر أيضا

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
