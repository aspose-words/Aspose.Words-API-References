---
title: ShapeBase.Title
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على أو تعيين العنوان التسمية التوضيحية لكائن الشكل الحالي.
type: docs
weight: 490
url: /ar/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

الحصول على أو تعيين العنوان (التسمية التوضيحية) لكائن الشكل الحالي.

```csharp
public string Title { get; set; }
```

### ملاحظات

الافتراضي هو سلسلة فارغة.

لا يمكن أن يكون فارغًا ، لكن يمكن أن يكون سلسلة فارغة.

### أمثلة

يوضح كيفية تعيين عنوان الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء شكل ، وأعطه عنوانًا ، ثم أضفه إلى المستند.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// عندما نحفظ مستندًا بشكل له عنوان ،
// Aspose.Words سيخزن هذا العنوان في النص البديل للشكل.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


