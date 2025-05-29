---
title: SoftEdgeFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نصف قطر SoftEdgeFormat لضبط تأثيرات الحواف الناعمة بسهولة. تحكم بدقة في طول نصف القطر لتحصل على نتائج بصرية مذهلة.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/softedgeformat/radius/
---
## SoftEdgeFormat.Radius property

يحصل على أو يعين قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). القيمة الافتراضية هي 0.0.

```csharp
public double Radius { get; set; }
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
