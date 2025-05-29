---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Stroke Color2 - قم بتعزيز تصميماتك باستخدام لون ضربة ثانية قابل للتخصيص للحصول على صور نابضة بالحياة وجذابة للنظر.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

يحدد لونًا ثانيًا للخط.

```csharp
public Color Color2 { get; set; }
```

## ملاحظات

القيمة الافتراضية لـ[`Shape`](../../shape/) هو White .

## أمثلة

يوضح كيفية معالجة ميزات شكل السكتة الدماغية.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// يمكن أن تحتوي الضربات على لونين، يتم استخدامهما لإنشاء نمط محدد بواسطة بيانات صورة ثنائية اللون.
// لا تستخدم الضربات ذات اللون الواحد خاصية Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### أنظر أيضا

* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
