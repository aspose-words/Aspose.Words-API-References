---
title: ReflectionFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words لـ .NET
description: اضبط شفافية ReflectionFormat من 0.0 (معتم) إلى 1.0 (شفاف) لتأثيرات انعكاس قابلة للتخصيص. حسّن تصميماتك بدقة!
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/reflectionformat/transparency/
---
## ReflectionFormat.Transparency property

يحصل على أو يعين قيمة مزدوجة بين 0.0 (غير شفاف) و1.0 (واضح) تمثل درجة الشفافية لتأثير الانعكاس. القيمة الافتراضية هي 0.0.

```csharp
public double Transparency { get; set; }
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
