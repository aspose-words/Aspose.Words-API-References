---
title: ShapeBase.AnchorLocked
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يحدد ما إذا كان رابط الشكل مقفلاً أم لا.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

يحدد ما إذا كان رابط الشكل مقفلاً أم لا.

```csharp
public bool AnchorLocked { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

له تأثير فقط على أشكال المستوى الأعلى.

تؤثر هذه الخاصية على سلوك نقطة ارتساء الشكل في Microsoft Word. عندما لا يتم تأمين نقطة الارتساء، يمكن أن يؤدي نقل الشكل في Microsoft Word إلى نقل نقطة ارتساء الشكل أيضًا.

### أمثلة

يوضح كيفية قفل أو إلغاء قفل رابط فقرة الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// اضبط الخاصية "AnchorLocked" على "true" لمنع ربط الشكل
// من التحرك عند تحريك الشكل في Microsoft Word.
// اضبط خاصية "AnchorLocked" على "خطأ" للسماح بأي حركة للشكل
// لتحريك نقطة الارتساء أيضًا إلى أي فقرة أخرى ينتهي الشكل بالقرب منها.
shape.AnchorLocked = anchorLocked;

// إذا لم يكن الشكل يحتوي على رمز ربط مرئي على يساره،
// سنحتاج إلى تمكين نقاط الارتساء المرئية عبر "الخيارات" -> "العرض" -> "مراسي الكائنات".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


