---
title: NodeRendererBase.SizeInPoints
second_title: Aspose.Words لمراجع .NET API
description: NodeRendererBase ملكية. الحصول على الحجم الفعلي للشكل بالنقاط .
type: docs
weight: 30
url: /ar/net/aspose.words.rendering/noderendererbase/sizeinpoints/
---
## NodeRendererBase.SizeInPoints property

الحصول على الحجم الفعلي للشكل بالنقاط .

```csharp
public SizeF SizeInPoints { get; }
```

### ملاحظات

تعرض هذه الخاصية الحجم الفعلي للمربع المحيط بالشكل (كما هو معروض في الصفحة). يأخذ الحجم في الاعتبار دوران الشكل (إن وجد).

### أمثلة

يوضح كيفية قياس الأشكال وقياسها.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// تحقق من حجم الصورة التي سينشئها كائن OfficeMath عند عرضها.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// قد تحتوي الأشكال ذات الأجزاء الشفافة على قيم مختلفة في خصائص "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// احصل على حجم الشكل بالبكسل ، مع تغيير الحجم الخطي إلى DPI محدد.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// احصل على حجم الشكل بالبكسل ، ولكن باستخدام DPI مختلف للأبعاد الأفقية والرأسية.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// قد تختلف الحدود المعتمة هنا أيضًا.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### أنظر أيضا

* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../noderendererbase/)
* المجسم [Aspose.Words](../../../)


