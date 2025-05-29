---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase AnchorLocked للتحكم في قفل المرساة للأشكال، مما يعزز استقرار التصميم ومرونته في مشاريعك.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

يحدد ما إذا كان مرساة الشكل مقفلة.

```csharp
public bool AnchorLocked { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

له تأثير فقط على الأشكال ذات المستوى الأعلى.

تؤثر هذه الخاصية على سلوك مرساة الشكل في Microsoft Word. عندما لا يتم قفل المرساة، فإن تحريك الشكل في Microsoft Word يمكن أن يؤدي إلى تحريك مرساة الشكل أيضًا.

## أمثلة

يوضح كيفية قفل أو إلغاء قفل مرساة الفقرة الخاصة بالشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// اضبط خاصية "AnchorLocked" على "true" لمنع تثبيت الشكل
// من التحرك عند تحريك الشكل في Microsoft Word.
// اضبط خاصية "AnchorLocked" على "false" للسماح بأي حركة للشكل
// لتحريك مرساة أيضًا إلى أي فقرة أخرى ينتهي الشكل بالقرب منها.
shape.AnchorLocked = anchorLocked;

// إذا لم يكن للشكل رمز مرساة مرئي على يساره،
// سوف نحتاج إلى تمكين المراسي المرئية عبر "الخيارات" -> "العرض" -> "مراسي الكائنات".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
