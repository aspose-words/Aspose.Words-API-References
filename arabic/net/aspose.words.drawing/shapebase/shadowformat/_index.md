---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase ShadowFormat لتحسين تصميماتك بتأثيرات ظل قابلة للتخصيص للأشكال. حسّن مظهرك اليوم!
type: docs
weight: 520
url: /ar/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

يحصل على تنسيق الظل للشكل.

```csharp
public ShadowFormat ShadowFormat { get; }
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

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
