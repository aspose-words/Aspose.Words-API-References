---
title: Stroke.Color2
second_title: Aspose.Words لمراجع .NET API
description: Stroke ملكية. يحدد اللون الثاني للحد.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

يحدد اللون الثاني للحد.

```csharp
public Color Color2 { get; set; }
```

### ملاحظات

القيمة الافتراضية ل[`Shape`](../../shape/) is White.

### أمثلة

يوضح كيفية معالجة ميزات حدود الشكل.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// يمكن أن تحتوي الحدود على لونين، يُستخدمان لإنشاء نمط محدد بواسطة بيانات الصورة ذات اللونين.
// لا تستخدم الحدود ذات اللون الواحد خاصية Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### أنظر أيضا

* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../stroke/)
* المجسم [Aspose.Words](../../../)


