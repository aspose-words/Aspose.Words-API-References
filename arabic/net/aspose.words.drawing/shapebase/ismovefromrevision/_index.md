---
title: ShapeBase.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase IsMoveFromRevision في مايكروسوفت وورد. تتبع التغييرات بسهولة وحدد الكائنات المنقولة أو المحذوفة بدقة.
type: docs
weight: 340
url: /ar/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات.

```csharp
public bool IsMoveFromRevision { get; }
```

## أمثلة

يوضح كيفية التعرف على أشكال مراجعة الحركة.

```csharp
// مراجعة النقل هي عندما نقوم بنقل عنصر في نص المستند عن طريق قصه ولصقه في Microsoft Word أثناء
// تتبع التغييرات. إذا أضفنا شكلًا مضمّنًا في حركة نص كهذه، فسيكون هذا الشكل أيضًا مراجعة.
// لا يؤدي نسخ ولصق أو نقل الأشكال العائمة إلى إنشاء مراجعات النقل.
Document doc = new Document(MyDir + "Revision shape.docx");

// تتكون مراجعات النقل من أزواج من مراجعات "النقل من" و"النقل إلى". نقلنا هذا المستند بشكل واحد،
// ولكن حتى نقبل أو نرفض تعديل الحركة، سيكون هناك حالتان من هذا الشكل.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// هذا هو الإصدار "نقل إلى"، وهو الشكل عند وجهة وصوله.
// إذا قبلنا المراجعة، فإن شكل المراجعة "نقل إلى" سيختفي،
// وسيظل شكل المراجعة "الانتقال من" كما هو.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// هذا هو الإصدار "الانتقال من"، وهو الشكل في موقعه الأصلي.
// إذا قبلنا المراجعة، فإن شكل المراجعة "الانتقال من" سيختفي،
// وسيظل شكل المراجعة "نقل إلى" كما هو.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
