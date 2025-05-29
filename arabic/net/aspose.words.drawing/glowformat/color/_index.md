---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "تنسيق الألوان المتوهجة" لتخصيص تأثيرات التوهج. حدّد ألوانًا زاهية بسهولة لتأثير بصري مذهل. اللون الافتراضي هو الأسود.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

يحصل على أو يعينColor الكائن الذي يمثل اللون لتأثير التوهج. القيمة الافتراضية هيBlack .

```csharp
public Color Color { get; set; }
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
