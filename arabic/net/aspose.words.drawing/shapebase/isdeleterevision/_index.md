---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase IsDeleteRevision، وتعلم كيفية إشارتها إلى حذف الكائن في Microsoft Word مع تمكين تتبع التغييرات لتحسين إدارة المستندات.
type: docs
weight: 270
url: /ar/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات.

```csharp
public bool IsDeleteRevision { get; }
```

## أمثلة

يوضح كيفية العمل مع أشكال المراجعة.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// قم بإدراج شكل مضمن دون تتبع المراجعات، مما سيجعل هذا الشكل ليس مراجعة من أي نوع.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// ابدأ بتتبع المراجعات ثم أدخل شكلًا آخر، والذي سيكون بمثابة مراجعة.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// نظرًا لأننا قمنا بإزالة هذا الشكل أثناء تتبع التغييرات،
// يظل الشكل موجودًا في المستند ويُحسب كمراجعة حذف.
// سيؤدي قبول هذه المراجعة إلى إزالة الشكل بشكل دائم، وسيؤدي رفضها إلى الاحتفاظ به في المستند.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// وقمنا بإدراج شكل آخر أثناء تتبع التغييرات، لذلك سيتم احتساب هذا الشكل كمراجعة إدراج.
// قبول هذه المراجعة سيؤدي إلى استيعاب هذا الشكل في المستند باعتباره غير مراجعة،
// ورفض المراجعة سيؤدي إلى إزالة هذا الشكل بشكل دائم.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
