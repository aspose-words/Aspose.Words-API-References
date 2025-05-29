---
title: SoftEdgeFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words لـ .NET
description: أزل SoftEdgeFormat بسهولة من الكائن الرئيسي باستخدام طريقة SoftEdgeFormat Remove. بسّط تصميمك لتحقيق أفضل النتائج!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat.Remove method

يزيل[`SoftEdgeFormat`](../) من الكائن الرئيسي.

```csharp
public void Remove()
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

* class [SoftEdgeFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
