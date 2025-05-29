---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShadowFormat Color لتخصيص ألوان الظل في تصميماتك. اللون الافتراضي هو الأسود، ولكن أطلق العنان لإبداعك مع خيارات نابضة بالحياة!
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

يحصل علىColor الكائن الذي يمثل لون الظل. القيمة الافتراضية هيBlack .

```csharp
public Color Color { get; }
```

## أمثلة

يوضح كيفية الحصول على لون الظل.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### أنظر أيضا

* class [ShadowFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
