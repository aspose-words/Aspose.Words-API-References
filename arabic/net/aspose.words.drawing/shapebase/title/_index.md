---
title: ShapeBase.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words لـ .NET
description: أدر خصائص عنوان ShapeBase بسهولة. عيّن أو استرجع عنوان أي شكل لتحسين وضوح تصميمك وجاذبيته.
type: docs
weight: 570
url: /ar/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

يحصل على عنوان (التعليق التوضيحي) لكائن الشكل الحالي أو يعينه.

```csharp
public string Title { get; set; }
```

## ملاحظات

افتراضيًا، السلسلة فارغة.

لا يمكن أن يكون`باطل`، ولكن يمكن أن تكون سلسلة فارغة.

## أمثلة

يوضح كيفية تعيين عنوان الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء شكل، وإعطائه عنوانًا، ثم قم بإضافته إلى المستند.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// عندما نحفظ مستندًا به شكل يحتوي على عنوان،
// سيقوم Aspose.Words بتخزين هذا العنوان في نص Alt الخاص بالشكل.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
