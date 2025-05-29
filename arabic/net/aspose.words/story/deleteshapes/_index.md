---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words لـ .NET
description: أزل جميع الأشكال من نص قصتك بسهولة باستخدام طريقة حذف الأشكال. بسّط محتواك وحسّن وضوحه اليوم!
type: docs
weight: 70
url: /ar/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

يحذف جميع الأشكال من نص هذه القصة.

```csharp
public void DeleteShapes()
```

## أمثلة

يوضح كيفية إزالة كافة الأشكال من العقدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمّن،
// والتي تحتوي على فقرة رئيسية، وهي عقدة فرعية لجسم القسم الأول.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

//يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا النص.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* class [Story](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
