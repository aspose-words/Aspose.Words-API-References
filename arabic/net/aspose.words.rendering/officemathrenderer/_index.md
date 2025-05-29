---
title: OfficeMathRenderer Class
linktitle: OfficeMathRenderer
articleTitle: OfficeMathRenderer
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Rendering.OfficeMathRenderer لتحويل OfficeMath بسهولة إلى صور نقطية أو متجهة مذهلة لمشاريعك.
type: docs
weight: 5290
url: /ar/net/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class

يوفر طرقًا لعرض فردي[`OfficeMath`](../../aspose.words.math/officemath/) إلى صورة نقطية أو متجهة أو إلى كائن رسومي.

لمعرفة المزيد، قم بزيارة[العمل مع OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) مقالة توثيقية.

```csharp
public class OfficeMathRenderer : NodeRendererBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OfficeMathRenderer](officemathrenderer/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | يحصل على الحدود الفعلية للشكل بالنقاط. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | يحصل على الحدود المعتمة للشكل بالنقاط. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | يحصل على الحجم الفعلي للشكل بالنقاط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float*) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float, float*) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float*) | يحسب الحدود المعتمة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float, float*) | يحسب الحدود المعتمة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float*) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float, float*) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | يعرض الشكل فيGraphics الكائن إلى مقياس محدد. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | يعرض الشكل فيGraphics الكائن إلى حجم محدد. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | يقوم بتحويل الشكل إلى صورة ويحفظه في مجرى. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | يقوم بتحويل الشكل إلى صورة SVG وحفظه في مجرى مائي. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | يقوم بتحويل الشكل إلى صورة ويحفظه في ملف. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | يقوم بتحويل الشكل إلى صورة SVG وحفظه في ملف. |

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

* class [NodeRendererBase](../noderendererbase/)
* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)
