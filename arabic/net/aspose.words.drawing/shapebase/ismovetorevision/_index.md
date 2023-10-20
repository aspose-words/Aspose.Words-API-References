---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words لـ .NET
description: ShapeBase IsMoveToRevision ملكية. إرجاعحقيقي إذا تم نقل هذا الكائن إدراجه في Microsoft Word أثناء تمكين تعقب التغييرات في C#.
type: docs
weight: 330
url: /ar/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsMoveToRevision { get; }
```

## أمثلة

يوضح كيفية التعرف على أشكال المراجعة المتحركة.

```csharp
// تتم مراجعة النقل عندما ننقل عنصرًا في نص المستند عن طريق قصه ولصقه في Microsoft Word أثناء
// تتبع التغييرات. إذا قمنا بإدراج شكل سطري في حركة النص هذه، فسيكون هذا الشكل بمثابة مراجعة أيضًا.
// لا يؤدي النسخ واللصق أو نقل الأشكال العائمة إلى إنشاء مراجعات متحركة.
Document doc = new Document(MyDir + "Revision shape.docx");

// نقل المراجعات يتكون من أزواج من المراجعات "الانتقال من" و"الانتقال إلى". لقد تحركنا في هذه الوثيقة بشكل واحد،
// ولكن حتى نقبل أو نرفض مراجعة النقل، سيكون هناك حالتان من هذا الشكل.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// هذه هي المراجعة "الانتقال إلى"، وهي الشكل عند وجهة وصوله.
// إذا قبلنا المراجعة، فسيختفي شكل المراجعة "الانتقال إلى" هذا،
// وسيظل شكل المراجعة "الانتقال من" موجودًا.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// هذه هي مراجعة "الانتقال من"، وهي الشكل في موقعه الأصلي.
// إذا قبلنا المراجعة، فسيختفي شكل المراجعة "الانتقال من"،
// وسيظل شكل المراجعة "الانتقال إلى" موجودًا.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
