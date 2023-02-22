---
title: ShapeBase.AnchorLocked
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يحدد ما إذا كانت نقطة ارتساء الشكل مؤمنة.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

يحدد ما إذا كانت نقطة ارتساء الشكل مؤمنة.

```csharp
public bool AnchorLocked { get; set; }
```

### ملاحظات

النظام الأساسي **خاطئة**.

له تأثير فقط لأشكال المستوى الأعلى.

تؤثر هذه الخاصية على سلوك ارتساء الشكل في Microsoft Word. عندما لا يتم تأمين نقطة الارتساء ، يمكن أن يؤدي تحريك الشكل في Microsoft Word إلى تحريك نقطة ارتساء الشكل أيضًا.

### أمثلة

يوضح كيفية قفل أو إلغاء قفل نقطة ارتساء فقرة الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// اضبط خاصية "AnchorLocked" على "true" لمنع ارتساء الشكل
// من التحرك عند نقل الشكل في Microsoft Word.
// اضبط خاصية "AnchorLocked" على "false" للسماح بأي حركة للشكل
// لتحريك نقطة الارتساء الخاصة بها إلى أي فقرة أخرى ينتهي بها الشكل بالقرب منها.
shape.AnchorLocked = anchorLocked;

// إذا كان الشكل لا يحتوي على رمز ارتساء مرئي على يساره ،
// سنحتاج إلى تمكين المراسي المرئية عبر "الخيارات" - >; "عرض" - >. "مرساة الكائن".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


