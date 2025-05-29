---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الشفافية في GlowFormat، واضبط تأثيرات التوهج بسهولة من معتم إلى شفاف (من 0.0 إلى 1.0) للحصول على تأثير بصري مذهل. الإعداد الافتراضي هو 0.0.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

يحصل على درجة الشفافية لتأثير التوهج أو يعينها كقيمة بين 0.0 (غير شفاف) و1.0 (واضح). القيمة الافتراضية هي 0.0.

```csharp
public double Transparency { get; set; }
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
