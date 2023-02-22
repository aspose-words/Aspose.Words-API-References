---
title: ShapeBase.IsMoveFromRevision
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. عوائد حقيقي إذا تم نقل حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.
type: docs
weight: 310
url: /ar/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsMoveFromRevision { get; }
```

### أمثلة

يوضح كيفية تحديد أشكال المراجعة المتحركة.

```csharp
// مراجعة الحركة هي عندما ننقل عنصرًا في نص المستند عن طريق قصه ولصقه في Microsoft Word أثناء ذلك
// تتبع التغييرات. إذا قمنا بإدخال شكل مضمن في حركة النص هذه ، فسيكون هذا الشكل أيضًا مراجعة.
// لا يؤدي نسخ الأشكال العائمة ولصقها أو نقلها إلى إنشاء مراجعات متحركة.
Document doc = new Document(MyDir + "Revision shape.docx");

// نقل المراجعات تتكون من أزواج من المراجعات "الانتقال من" و "الانتقال إلى". انتقلنا في هذا المستند في شكل واحد ،
// ولكن حتى نقبل أو نرفض مراجعة النقل ، ستكون هناك حالتان من هذا الشكل.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// هذه هي مراجعة "الانتقال إلى" ، وهي الشكل عند وجهة وصولها.
// إذا قبلنا المراجعة ، فسيختفي شكل المراجعة "الانتقال إلى" ،
// وسيظل شكل المراجعة "الانتقال من".
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// هذه هي مراجعة "الانتقال من" ، وهي الشكل الموجود في موقعه الأصلي.
// إذا قبلنا المراجعة ، فسيختفي شكل المراجعة "الانتقال من" ،
// وسيظل شكل المراجعة "نقل إلى".
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


