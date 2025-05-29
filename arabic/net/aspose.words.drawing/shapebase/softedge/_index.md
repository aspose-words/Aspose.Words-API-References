---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: Aspose.Words لـ .NET
description: حسّن تصميماتك مع ShapeBase SoftEdge لتنسيق حواف سلس وناعم. حسّن صورك بسلاسة وتميّز في كل مشروع!
type: docs
weight: 550
url: /ar/net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

يحصل على تنسيق الحافة الناعمة للشكل.

```csharp
public SoftEdgeFormat SoftEdge { get; }
```

## أمثلة

يوضح كيفية تعيين حد لدقة الصورة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

يوضح كيفية العمل مع تنسيق الحافة الناعمة.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// قم بتطبيق حافة ناعمة على الشكل.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// قم بتحميل المستند على شكل مستطيل ذو حافة ناعمة.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

//تحقق من نصف قطر الحافة الناعمة.
Assert.AreEqual(30, softEdgeFormat.Radius);

// قم بإزالة الحافة الناعمة من الشكل.
softEdgeFormat.Remove();

//تحقق من نصف قطر الحافة الناعمة التي تمت إزالتها.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### أنظر أيضا

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
