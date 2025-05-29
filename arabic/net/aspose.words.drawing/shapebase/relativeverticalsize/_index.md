---
title: ShapeBase.RelativeVerticalSize
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase RelativeVerticalSize لضبط الأبعاد الرأسية للأشكال بسهولة لتحسين مرونة التصميم ودقته.
type: docs
weight: 480
url: /ar/net/aspose.words.drawing/shapebase/relativeverticalsize/
---
## ShapeBase.RelativeVerticalSize property

يحصل على قيمة الحجم النسبي للشكل في الاتجاه الرأسي أو يعينها.

```csharp
public RelativeVerticalSize RelativeVerticalSize { get; set; }
```

## ملاحظات

القيمة الافتراضية هيMargin.

لا يكون له تأثير إلا إذا[`HeightRelative`](../heightrelative/) تم تعيينه.

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

* enum [RelativeVerticalSize](../../relativeverticalsize/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
