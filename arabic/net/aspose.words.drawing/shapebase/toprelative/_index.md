---
title: ShapeBase.TopRelative
linktitle: TopRelative
articleTitle: TopRelative
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase TopRelative لإدارة موضع الشكل بسهولة. اضبط تصميمك بدقة باستخدام قيم النسبة المئوية العليا للحصول على تخطيط مثالي.
type: docs
weight: 590
url: /ar/net/aspose.words.drawing/shapebase/toprelative/
---
## ShapeBase.TopRelative property

يحصل على القيمة التي تمثل الموضع العلوي النسبي للشكل كنسبة مئوية أو يعينها.

```csharp
public float TopRelative { get; set; }
```

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

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
