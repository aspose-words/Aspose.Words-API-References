---
title: Class OfficeMathRenderer
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Rendering.OfficeMathRenderer فصل. يوفر طرقًا لتمثيل الفردOfficeMath إلى صورة نقطية أو متجهة أو إلى كائن رسومي.
type: docs
weight: 4560
url: /ar/net/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class

يوفر طرقًا لتمثيل الفرد[`OfficeMath`](../../aspose.words.math/officemath/) إلى صورة نقطية أو متجهة أو إلى كائن رسومي.

لمعرفة المزيد، قم بزيارة[العمل مع OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) مقالة توثيقية.

```csharp
public class OfficeMathRenderer : NodeRendererBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OfficeMathRenderer](officemathrenderer/)(OfficeMath) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | الحصول على الحدود الفعلية للشكل بالنقاط. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | الحصول على الحدود المعتمة للشكل بالنقاط. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | الحصول على الحجم الفعلي للشكل بالنقاط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(float, float) | حساب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(float, float, float) | حساب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(float, float) | حساب الحدود المعتمة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(float, float, float) | حساب الحدود المعتمة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(float, float) | حساب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(float, float, float) | حساب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(Graphics, float, float, float) | يحول الشكل إلى aGraphics كائن بمقياس محدد. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(Graphics, float, float, float, float) | يحول الشكل إلى aGraphics كائن بحجم محدد. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(Stream, ImageSaveOptions) | يعرض الشكل في صورة ويحفظ في دفق. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(string, ImageSaveOptions) | يحول الشكل إلى صورة ويحفظ في ملف. |

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

* class [NodeRendererBase](../noderendererbase/)
* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)


