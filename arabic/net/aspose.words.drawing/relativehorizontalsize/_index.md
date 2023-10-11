---
title: Enum RelativeHorizontalSize
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.RelativeHorizontalSize تعداد. يحدد نسبيًا ما يتم حساب عرض الشكل أو إطار النص أفقيًا.
type: docs
weight: 1200
url: /ar/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

يحدد نسبيًا ما يتم حساب عرض الشكل أو إطار النص أفقيًا.

```csharp
public enum RelativeHorizontalSize
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Margin | `0` | يحدد أن العرض يتم حسابه نسبيًا للمسافة بين الهامش الأيسر والأيمن. |
| Page | `1` | يحدد أن العرض يتم حسابه نسبيًا لعرض الصفحة. |
| LeftMargin | `2` | يحدد أن العرض يتم حسابه نسبيًا لحجم مساحة الهامش الأيسر. |
| RightMargin | `3` | يحدد أن العرض يتم حسابه نسبيًا لحجم مساحة الهامش الصحيح. |
| InnerMargin | `4` | يحدد أن العرض يتم حسابه نسبيًا إلى حجم مساحة الهامش الداخلي، إلى حجم مساحة الهامش الأيسر للصفحات الفردية وإلى حجم مساحة الهامش الأيمن للصفحات الزوجية. |
| OuterMargin | `5` | يحدد أن العرض يتم حسابه نسبيًا لحجم مساحة الهامش الخارجي، لحجم مساحة الهامش الأيمن للصفحات الفردية وحجم مساحة الهامش الأيسر للصفحات الزوجية. |
| Default | `1` | القيمة الافتراضية هيMargin . |

### أمثلة

يوضح كيفية ضبط الحجم والموضع النسبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إضافة شكل بسيط بالحجم والموضع المطلقين.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// قم بتعيين WrapType على WrapType.None حيث يتم تحويل الأشكال المضمنة تلقائيًا إلى وحدات مطلقة.
shape.WrapType = WrapType.None;

// التحقق من الحجم الأفقي النسبي وتعيينه.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // ضبط الحجم الأفقي للربط بالهامش.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // ضبط العرض على 50% من عرض الهامش.
    shape.WidthRelative = 50;
}

// التحقق من الحجم الرأسي النسبي وتعيينه.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // ضبط الحجم الرأسي للربط بالهامش.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // ضبط الارتفاع على 30% من ارتفاع الهامش.
    shape.HeightRelative = 30;
}

// التحقق من الوضع الرأسي النسبي وتعيينه.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // تحديد الموضع المرتبط بـ TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // تعيين أعلى نسبة إلى 30% من موضع الهامش العلوي.
    shape.TopRelative = 30;
}

// التحقق من الوضع الأفقي النسبي وضبطه.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // تعيين موضع ربط RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // يمكن أن تكون القيمة النسبية للموضع سالبة.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### أنظر أيضا

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


