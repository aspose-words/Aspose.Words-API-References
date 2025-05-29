---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Drawing.GlowFormat لتحسين مستنداتك بتأثيرات توهج مذهلة. ارتقِ بتصميمك مع خيارات تنسيق فريدة!
type: docs
weight: 1300
url: /ar/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

يمثل تنسيق التوهج لكائن.

```csharp
public class GlowFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | يحصل على أو يعينColor الكائن الذي يمثل اللون لتأثير التوهج. القيمة الافتراضية هيBlack . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | يحصل على أو يعين قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). القيمة الافتراضية هي 0.0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | يحصل على درجة الشفافية لتأثير التوهج أو يعينها كقيمة بين 0.0 (غير شفاف) و1.0 (واضح). القيمة الافتراضية هي 0.0. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | يزيل`GlowFormat` من الكائن الرئيسي. |

## ملاحظات

استخدم[`Glow`](../shapebase/glow/) الخاصية للوصول إلى خصائص التوهج الخاصة بالكائن. لا تقم بإنشاء مثيلات من`GlowFormat` الصف مباشرة.

## أمثلة

يوضح كيفية التفاعل مع تأثير شكل التوهج.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
