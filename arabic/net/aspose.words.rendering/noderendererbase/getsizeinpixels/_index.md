---
title: NodeRendererBase.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة NodeRendererBase GetSizeInPixels لحساب أبعاد الشكل بالبكسل بدقة بناءً على عامل التكبير والدقة. حسّن تصميماتك!
type: docs
weight: 60
url: /ar/net/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| scale | Single | عامل التكبير (1.0 هو 100%). |
| dpi | Single | الدقة (الأفقية والرأسية) لتحويل النقاط إلى بكسل (نقطة لكل بوصة). |

### قيمة الإرجاع

حجم الشكل بالبكسل.

## ملاحظات

هذه الطريقة تحول[`SizeInPoints`](../sizeinpoints/) يتم تحويل الشكل إلى حجم بالبكسل، ومن المفيد استخدام x000d_ عندما تريد إنشاء خريطة نقطية لعرض الشكل بشكل أنيق على خريطة النقطية.

## أمثلة

يوضح كيفية قياس الأشكال وتغيير حجمها.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// التحقق من حجم الصورة التي سيقوم كائن OfficeMath بإنشائها عند عرضها.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// قد تحتوي الأشكال ذات الأجزاء الشفافة على قيم مختلفة في خصائص "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// احصل على حجم الشكل بالبكسل، مع التدرج الخطي إلى DPI محدد.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// احصل على حجم الشكل بالبكسل، ولكن مع DPI مختلف للأبعاد الأفقية والرأسية.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

//قد تختلف الحدود المعتمة هنا أيضًا.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### أنظر أيضا

* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| scale | Single | عامل التكبير (1.0 هو 100%). |
| horizontalDpi | Single | الدقة الأفقية لتحويل النقاط إلى بكسل (نقطة لكل بوصة). |
| verticalDpi | Single | الدقة الرأسية لتحويل النقاط إلى بكسل (نقطة لكل بوصة). |

### قيمة الإرجاع

حجم الشكل بالبكسل.

## ملاحظات

هذه الطريقة تحول[`SizeInPoints`](../sizeinpoints/) يتم تحويل الشكل إلى حجم بالبكسل، ومن المفيد استخدام x000d_ عندما تريد إنشاء خريطة نقطية لعرض الشكل بشكل أنيق على خريطة النقطية.

## أمثلة

يوضح كيفية قياس الأشكال وتغيير حجمها.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// التحقق من حجم الصورة التي سيقوم كائن OfficeMath بإنشائها عند عرضها.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// قد تحتوي الأشكال ذات الأجزاء الشفافة على قيم مختلفة في خصائص "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// احصل على حجم الشكل بالبكسل، مع التدرج الخطي إلى DPI محدد.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// احصل على حجم الشكل بالبكسل، ولكن مع DPI مختلف للأبعاد الأفقية والرأسية.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

//قد تختلف الحدود المعتمة هنا أيضًا.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### أنظر أيضا

* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
