---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase IsInline للتحقق بسهولة مما إذا كان الشكل الخاص بك يتماشى مع النص، مما يعمل على تحسين التصميم الخاص بك وتحسين كفاءة التخطيط.
type: docs
weight: 310
url: /ar/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

طريقة سريعة لتحديد ما إذا كان هذا الشكل موضوعًا في خط واحد مع النص.

```csharp
public bool IsInline { get; }
```

## ملاحظات

له تأثير فقط على الأشكال ذات المستوى الأعلى.

## أمثلة

يوضح كيفية تحديد ما إذا كان الشكل مضمنًا أم عائمًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان من التغليف الذي قد تمتلكه الأشكال.
// 1 - مضمن:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// يقع الشكل المضمن داخل فقرة بين عناصر فقرة أخرى، مثل سلاسل النصوص.
// في Microsoft Word، يمكننا النقر فوق الشكل وسحبه إلى أي فقرة كما لو كان حرفًا.
// إذا كان الشكل كبيرًا، فسوف يؤثر على التباعد الرأسي للفقرات.
//لا يمكننا نقل هذا الشكل إلى مكان لا يحتوي على فقرة.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - عائم:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// الشكل العائم ينتمي إلى الفقرة التي نقوم بإدراجه فيها،
// والذي يمكننا تحديده من خلال رمز المرساة الذي يظهر عندما نضغط على الشكل.
// إذا لم يكن للشكل رمز مرساة مرئي على يساره،
// سوف نحتاج إلى تمكين المراسي المرئية عبر "الخيارات" -> "العرض" -> "مراسي الكائنات".
// في Microsoft Word، يمكننا النقر بزر الماوس الأيسر وسحب هذا الشكل بحرية إلى أي مكان.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
