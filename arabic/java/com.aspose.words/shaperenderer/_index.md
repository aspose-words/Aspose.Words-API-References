---
title: "ShapeRenderer"
linktitle: "ShapeRenderer"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا لتصوير شكل فردي أو GroupShape إلى صورة نقطية أو متجهة أو إلى كائن Graphics في Java."
type: docs
weight: 616
url: /ar/java/com.aspose.words/shaperenderer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeRendererBase](../../com.aspose.words/noderendererbase/)
```
public class ShapeRenderer extends NodeRendererBase
```

يوفر طرقًا لتصوير عنصر [Shape](../../com.aspose.words/shape/) أو [GroupShape](../../com.aspose.words/groupshape/) إلى صورة نقطية أو متجهة أو إلى كائن Graphics.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Shapes ][Working with Shapes].


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ShapeRenderer(ShapeBase shape)](#ShapeRenderer-com.aspose.words.ShapeBase) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [getBoundsInPoints()](#getBoundsInPoints) | يحصل على الحدود الفعلية للشكل بالنقاط. |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints) | يحصل على الحدود غير الشفافة للشكل بالنقاط. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [getSizeInPoints()](#getSizeInPoints) | يحصل على الحجم الفعلي للشكل بالنقاط. |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float) | يرسم الشكل داخل كائن java.awt.Graphics2D إلى مقياس محدد. |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float) | يرسم الشكل داخل كائن java.awt.Graphics2D إلى حجم محدد. |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions) |  |
| [save(OutputStream stream, SvgSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions) | يرسم الشكل ويحفظه كصورة. |
| [save(String fileName, SvgSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SvgSaveOptions) | يرسم الشكل ويحفظه كصورة SVG. |
### ShapeRenderer(ShapeBase shape) {#ShapeRenderer-com.aspose.words.ShapeBase}
```
public ShapeRenderer(ShapeBase shape)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shape | [ShapeBase](../../com.aspose.words/shapebase/) | كائن الشكل DrawinML الذي تريد تصويره. |

### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين.

 **Remarks:** 

هذه الطريقة تحول [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) إلى مستطيل بالبكسل.

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| dpi | float | الدقة (الأفقية والعمودية) لتحويل النقاط إلى بكسل (نقطة في البوصة). |

**Returns:**
java.awt.Rectangle - الصندوق المحيط الفعلي (كما يُرسم على الصفحة) للشكل بالبكسل.
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين.

 **Remarks:** 

هذه الطريقة تحول [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) إلى مستطيل بالبكسل.

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| horizontalDpi | float | الدقة الأفقية لتحويل النقاط إلى بكسل (نقطة في البوصة). |
| verticalDpi | float | الدقة العمودية لتحويل النقاط إلى بكسل (نقطة في البوصة). |

**Returns:**
java.awt.Rectangle - الصندوق المحيط الفعلي (كما يُرسم على الصفحة) للشكل بالبكسل.
### getBoundsInPoints() {#getBoundsInPoints}
```
public Rectangle2D.Float getBoundsInPoints()
```


يحصل على الحدود الفعلية للشكل بالنقاط.

 **Remarks:** 

هذه الخاصية تُعيد الصندوق المحيط الفعلي (كما يُرسم على الصفحة) للشكل. تأخذ الحدود في الاعتبار دوران الشكل (إن وجد).

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - الحدود الفعلية للشكل بالنقاط.
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين.

 **Remarks:** 

هذه الطريقة تحول [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) إلى مستطيل بالبكسل وتكون مفيدة عندما تريد إنشاء صورة نقطية لتصيير الشكل مع الجزء غير الشفاف فقط من الشكل.

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| dpi | float | الدقة للتحويل من النقاط إلى البكسل (نقطة في البوصة). |

**Returns:**
java.awt.Rectangle - المستطيل غير الشفاف للشكل بالبكسل.
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين.

 **Remarks:** 

هذه الطريقة تحول [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) إلى مستطيل بالبكسل وتكون مفيدة عندما تريد إنشاء صورة نقطية لتصيير الشكل مع الجزء غير الشفاف فقط من الشكل.

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| horizontalDpi | float | الدقة الأفقية لتحويل النقاط إلى بكسل (نقطة في البوصة). |
| verticalDpi | float | الدقة العمودية لتحويل النقاط إلى بكسل (نقطة في البوصة). |

**Returns:**
java.awt.Rectangle - المستطيل غير الشفاف للشكل بالبكسل.
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


يحصل على الحدود غير الشفافة للشكل بالنقاط.

 **Remarks:** 

هذه الخاصية تُعيد الصندوق المحيط غير الشفاف (أي يتم تجاهل الأجزاء الشفافة من الشكل) للشكل. يأخذ الصندوق في الاعتبار دوران الشكل.

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - الحدود غير الشفافة للشكل بالنقاط.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين.

 **Remarks:** 

هذه الطريقة تحول [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) إلى حجم بالبكسل وتكون مفيدة عندما تريد إنشاء صورة نقطية لتصيير الشكل بدقة على الصورة النقطية.

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| dpi | float | الدقة (الأفقية والعمودية) لتحويل النقاط إلى بكسل (نقطة في البوصة). |

**Returns:**
java.awt.Dimension - حجم الشكل بالبكسل.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين.

 **Remarks:** 

هذه الطريقة تحول [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) إلى حجم بالبكسل وتكون مفيدة عندما تريد إنشاء صورة نقطية لتصيير الشكل بدقة على الصورة النقطية.

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| horizontalDpi | float | الدقة الأفقية لتحويل النقاط إلى بكسل (نقطة في البوصة). |
| verticalDpi | float | الدقة العمودية لتحويل النقاط إلى بكسل (نقطة في البوصة). |

**Returns:**
java.awt.Dimension - حجم الشكل بالبكسل.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


يحصل على الحجم الفعلي للشكل بالنقاط.

 **Remarks:** 

هذه الخاصية تُعيد حجم الصندوق المحيط الفعلي (كما يُصَّر على الصفحة) للشكل. يأخذ الحجم في الاعتبار دوران الشكل (إن وجد).

 **Examples:** 

يعرض كيفية قياس وتكبير الأشكال.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Point2D.Float - الحجم الفعلي للشكل بالنقاط.
### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


يرسم الشكل داخل كائن java.awt.Graphics2D إلى مقياس محدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الرسومات | java.awt.Graphics2D | الكائن الذي يتم التصيير إليه. |
| x | float | إحداثي X (بالوحدات العالمية) للزاوية العلوية اليسرى للشكل المُصَّر. |
| y | float | إحداثي Y (بالوحدات العالمية) للزاوية العلوية اليسرى للشكل المُصَّر. |
| المقياس | float | المقياس لتصيير الشكل (1.0 يساوي 100%). |

**Returns:**
java.awt.geom.Point2D.Float - العرض والارتفاع (بالوحدات العالمية) للشكل المُصَّر.
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


يرسم الشكل داخل كائن java.awt.Graphics2D إلى حجم محدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الرسومات | java.awt.Graphics2D | الكائن الذي يتم التصيير إليه. |
| x | float | إحداثي X (بالوحدات العالمية) للزاوية العلوية اليسرى للشكل المُصَّر. |
| y | float | إحداثي Y (بالوحدات العالمية) للزاوية العلوية اليسرى للشكل المُصَّر. |
| العرض | float | العرض الأقصى (بالوحدات العالمية) الذي يمكن أن يشغله الشكل المُصَّر. |
| الارتفاع | float | الارتفاع الأقصى (بالوحدات العالمية) الذي يمكن أن يشغله الشكل المُصَّر. |

**Returns:**
float - المقياس الذي تم حسابه تلقائيًا لتناسب الشكل المُصَّر الحجم المحدد.
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |

### save(OutputStream stream, SvgSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions}
```
public void save(OutputStream stream, SvgSaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


يقوم بتصيير الشكل وحفظه في صورة.  يصيّر الشكل في صورة ويحفظه في ملف.

 **Examples:** 

يوضح كيفية تصيير كائن Office Math في ملف صورة على نظام الملفات المحلي.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
 // how it renders the OfficeMath node into an image.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Scale" property to 5 to render the object to five times its original size.
 saveOptions.setScale(5f);

 math.getMathRenderer().save(getArtifactsDir() + "Shape.RenderOfficeMath.png", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be null. |

### save(String fileName, SvgSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SvgSaveOptions}
```
public void save(String fileName, SvgSaveOptions saveOptions)
```


Renders the shape and saves into an SVG image. Renders the shape into an SVG image and saves into a file.

 **Examples:** 

Shows how to pass save options when rendering office math.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath)doc.getChild(NodeType.OFFICE_MATH, 0, true);

 SvgSaveOptions options = new SvgSaveOptions();
 options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);

 math.getMathRenderer().save(getArtifactsDir() + "SvgSaveOptions.Output.svg", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be null. |

