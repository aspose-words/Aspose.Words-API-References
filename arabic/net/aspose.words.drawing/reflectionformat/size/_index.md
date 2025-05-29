---
title: ReflectionFormat.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية حجم تنسيق الانعكاس، وتحكم في حجم الانعكاس (0.0-1.0) للحصول على تأثيرات بصرية مذهلة في تصميماتك. حسّن جمالية مشروعك!
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/reflectionformat/size/
---
## ReflectionFormat.Size property

يحصل على أو يعين قيمة مزدوجة بين 0.0 و1.0 تمثل حجم reflection كنسبة مئوية من الكائن المنعكس. القيمة الافتراضية هي 0.0.

```csharp
public double Size { get; set; }
```

## أمثلة

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### أنظر أيضا

* class [ReflectionFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
