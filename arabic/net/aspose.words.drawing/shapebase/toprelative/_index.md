---
title: ShapeBase.TopRelative
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على أو تعيين القيمة التي تمثل الموضع العلوي النسبي للشكل بالنسبة المئوية.
type: docs
weight: 550
url: /ar/net/aspose.words.drawing/shapebase/toprelative/
---
## ShapeBase.TopRelative property

الحصول على أو تعيين القيمة التي تمثل الموضع العلوي النسبي للشكل بالنسبة المئوية.

```csharp
public float TopRelative { get; set; }
```

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

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


