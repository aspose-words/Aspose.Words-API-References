---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.ReflectionFormat لتنسيق انعكاس الكائنات المتقدم. حسّن تصميم مستندك بتكامل سلس!
type: docs
weight: 1570
url: /ar/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

يمثل تنسيق الانعكاس لكائن.

```csharp
public class ReflectionFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | يحصل على قيمة مزدوجة أو يعينها لتحديد درجة تأثير التمويه المطبق على تأثير الانعكاس بالنقاط. القيمة الافتراضية هي 0.0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | يحصل على قيمة مزدوجة أو يعينها لتحديد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. القيمة الافتراضية هي 0.0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | يحصل على أو يعين قيمة مزدوجة بين 0.0 و1.0 تمثل حجم reflection كنسبة مئوية من الكائن المنعكس. القيمة الافتراضية هي 0.0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | يحصل على أو يعين قيمة مزدوجة بين 0.0 (غير شفاف) و1.0 (واضح) تمثل درجة الشفافية لتأثير الانعكاس. القيمة الافتراضية هي 0.0. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | يزيل`ReflectionFormat` من الكائن الرئيسي. |

## ملاحظات

استخدم[`Reflection`](../shapebase/reflection/) الخاصية للوصول إلى خصائص الانعكاس لكائن. لا تقم بإنشاء مثيلات من`ReflectionFormat` الصف مباشرة.

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
