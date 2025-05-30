---
title: GlowFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نصف قطر تنسيق التوهج لتخصيص تأثيرات التوهج. اضبط نصف القطر بالنقاط لتحسينات بصرية مذهلة. القيمة الافتراضية 0.0.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/glowformat/radius/
---
## GlowFormat.Radius property

يحصل على أو يعين قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). القيمة الافتراضية هي 0.0.

```csharp
public double Radius { get; set; }
```

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

* class [GlowFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
