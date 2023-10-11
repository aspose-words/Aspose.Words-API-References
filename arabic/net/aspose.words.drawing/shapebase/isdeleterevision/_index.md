---
title: ShapeBase.IsDeleteRevision
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.
type: docs
weight: 250
url: /ar/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsDeleteRevision { get; }
```

### أمثلة

يوضح كيفية العمل مع أشكال المراجعة.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// قم بإدراج شكل سطري دون تتبع المراجعات، مما يجعل هذا الشكل ليس مراجعة من أي نوع.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// ابدأ بتتبع المراجعات، ثم أدخل شكلاً آخر، والذي سيكون بمثابة مراجعة.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// منذ أن قمنا بإزالة هذا الشكل بينما كنا نتتبع التغييرات،
// يستمر الشكل في المستند ويتم احتسابه كمراجعة حذف.
// سيؤدي قبول هذه المراجعة إلى إزالة الشكل نهائيًا، وسيؤدي رفضها إلى إبقائه في المستند.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// وقمنا بإدراج شكل آخر أثناء تتبع التغييرات، بحيث يتم احتساب هذا الشكل كمراجعة للإدراج.
// سيؤدي قبول هذه المراجعة إلى استيعاب هذا الشكل في المستند باعتباره غير مراجعة،
// ورفض المراجعة سيؤدي إلى إزالة هذا الشكل نهائيًا.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


