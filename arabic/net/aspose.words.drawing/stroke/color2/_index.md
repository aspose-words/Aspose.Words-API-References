---
title: Stroke.Color2
second_title: Aspose.Words لمراجع .NET API
description: Stroke ملكية. يحدد لونًا ثانيًا لحد .
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

يحدد لونًا ثانيًا لحد .

```csharp
public Color Color2 { get; set; }
```

### ملاحظات

القيمة الافتراضية لـ[`Shape`](../../shape/) هو White.

### أمثلة

يوضح كيفية معالجة ميزات ضربات الفرشاة.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// يمكن أن تحتوي السكتات الدماغية على لونين ، يتم استخدامهما لإنشاء نمط محدد ببيانات صور ثنائية اللون.
// السكتات الدماغية ذات اللون الواحد لا تستخدم خاصية Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### أنظر أيضا

* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../stroke/)
* المجسم [Aspose.Words](../../../)


