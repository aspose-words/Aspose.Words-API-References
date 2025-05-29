---
title: ReflectionFormat.Distance
linktitle: Distance
articleTitle: Distance
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية مسافة تنسيق الانعكاس، واضبط بسهولة فصل صورتك المنعكسة بالنقاط للحصول على تأثيرات بصرية مذهلة. القيمة الافتراضية هي 0.0.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/reflectionformat/distance/
---
## ReflectionFormat.Distance property

يحصل على قيمة مزدوجة أو يعينها لتحديد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. القيمة الافتراضية هي 0.0.

```csharp
public double Distance { get; set; }
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
