---
title: Story.DeleteShapes
second_title: Aspose.Words لمراجع .NET API
description: Story طريقة. حذف جميع الأشكال من نص هذه القصة.
type: docs
weight: 70
url: /ar/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

حذف جميع الأشكال من نص هذه القصة.

```csharp
public void DeleteShapes()
```

### أمثلة

يوضح كيفية إزالة كافة الأشكال من العقدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم DocumentBuilder لإدراج شكل. وهذا شكل خطي
// التي تحتوي على فقرة أصل، وهي عقدة فرعية لنص القسم الأول.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا الجسم.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* class [Story](../)
* مساحة الاسم [Aspose.Words](../../story/)
* المجسم [Aspose.Words](../../../)


