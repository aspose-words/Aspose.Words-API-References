---
title: NodeRendererBase.BoundsInPoints
second_title: Aspose.Words لمراجع .NET API
description: NodeRendererBase ملكية. الحصول على الحدود الفعلية للشكل بالنقاط.
type: docs
weight: 10
url: /ar/net/aspose.words.rendering/noderendererbase/boundsinpoints/
---
## NodeRendererBase.BoundsInPoints property

الحصول على الحدود الفعلية للشكل بالنقاط.

```csharp
public RectangleF BoundsInPoints { get; }
```

### ملاحظات

تُرجع هذه الخاصية المربع المحيط الفعلي (كما هو معروض على الصفحة) للشكل. تأخذ الحدود في الاعتبار تدوير الشكل (إن وجد).

### أمثلة

يوضح كيفية قياس الأشكال وحجمها.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// تحقق من حجم الصورة التي سينشئها كائن OfficeMath عندما نقوم بعرضها.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// قد تحتوي الأشكال ذات الأجزاء الشفافة على قيم مختلفة في خصائص "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// احصل على حجم الشكل بالبكسل، مع القياس الخطي إلى DPI محدد.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// احصل على حجم الشكل بالبكسل، ولكن مع DPI مختلفة للأبعاد الأفقية والرأسية.
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


