---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words لـ .NET
description: ShapeBase IsInline ملكية. طريقة سريعة لتحديد ما إذا كان هذا الشكل تم وضعه سطريًا مع النص في C#.
type: docs
weight: 290
url: /ar/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

طريقة سريعة لتحديد ما إذا كان هذا الشكل تم وضعه سطريًا مع النص.

```csharp
public bool IsInline { get; }
```

## ملاحظات

له تأثير فقط على أشكال المستوى الأعلى.

## أمثلة

يوضح كيفية تحديد ما إذا كان الشكل سطريًا أم عائمًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان من الالتفاف الذي قد تحتوي عليه الأشكال.
// 1 - مضمنة:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// يوجد شكل سطري داخل الفقرة بين عناصر الفقرة الأخرى، مثل أجزاء النص.
// في Microsoft Word، يمكننا النقر على الشكل وسحبه إلى أي فقرة كما لو كان حرفًا.
// إذا كان الشكل كبيرًا، فسيؤثر ذلك على التباعد العمودي بين الفقرات.
// لا يمكننا نقل هذا الشكل إلى مكان لا يحتوي على فقرة.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - العائمة:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// الشكل العائم ينتمي إلى الفقرة التي قمنا بإدراجه فيها،
// والذي يمكننا تحديده من خلال رمز الربط الذي يظهر عندما ننقر على الشكل.
// إذا لم يكن الشكل يحتوي على رمز ربط مرئي على يساره،
// سنحتاج إلى تمكين نقاط الارتساء المرئية عبر "الخيارات" -> "العرض" -> "مراسي الكائنات".
// في Microsoft Word، يمكننا النقر بزر الماوس الأيسر على هذا الشكل وسحبه بحرية إلى أي مكان.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
