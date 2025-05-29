---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة الحفظ في NodeRendererBase. قدّم الأشكال بسهولة كصور واحفظها في ملفات لضمان تكامل سلس وإنتاجية أفضل.
type: docs
weight: 90
url: /ar/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

يقوم بتحويل الشكل إلى صورة ويحفظه في ملف.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الصورة. إذا كان الملف موجودًا بالفعل بالاسم المحدد، فسيتم استبداله. |
| saveOptions | ImageSaveOptions | يحدد الخيارات التي تتحكم في كيفية عرض الشكل وحفظه. يمكن`باطل`. |

## أمثلة

يوضح كيفية تحويل كائن Office Math إلى ملف صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// قم بإنشاء كائن "ImageSaveOptions" لتمريره إلى طريقة "Save" الخاصة بمقدم العقدة لتعديلها
// كيف يتم تحويل عقدة OfficeMath إلى صورة.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// اضبط خاصية "المقياس" على 5 لجعل الكائن أكبر بخمس مرات من حجمه الأصلي.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

يقوم بتحويل الشكل إلى صورة SVG وحفظه في ملف.

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الصورة. إذا كان الملف موجودًا بالفعل بالاسم المحدد، فسيتم استبداله. |
| saveOptions | SvgSaveOptions | يحدد الخيارات التي تتحكم في كيفية عرض الشكل وحفظه. يمكن`باطل`. |

## أمثلة

يوضح كيفية تمرير خيارات الحفظ عند عرض الرياضيات في Office.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### أنظر أيضا

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

يقوم بتحويل الشكل إلى صورة ويحفظه في مجرى.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | المكان الذي سيتم فيه حفظ صورة الشكل. |
| saveOptions | ImageSaveOptions | يحدد الخيارات التي تتحكم في كيفية عرض الشكل وحفظه. يمكن`باطل` . إذا كان هذا هو`باطل`سيتم حفظ الصورة بتنسيق PNG. |

## أمثلة

يوضح كيفية استخدام برنامج عرض الأشكال لتصدير الأشكال إلى ملفات في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// يوجد 7 أشكال في المستند، بما في ذلك شكل مجموعة واحد مع شكلين فرعيين.
// سنقوم بتحويل كل شكل إلى ملف صورة في نظام الملفات المحلي
// مع تجاهل أشكال المجموعة لأنها ليس لها مظهر.
// سيؤدي هذا إلى إنتاج 6 ملفات صور.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

يقوم بتحويل الشكل إلى صورة SVG وحفظه في مجرى مائي.

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي سيتم فيه حفظ صورة SVG للشكل. |
| saveOptions | SvgSaveOptions | يحدد الخيارات التي تتحكم في كيفية عرض الشكل وحفظه. يمكن`باطل` . إذا كان هذا هو`باطل`سيتم حفظ الصورة بالخيارات الافتراضية. |

## أمثلة

يوضح كيفية تمرير خيارات الحفظ عند عرض الرياضيات في Office.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### أنظر أيضا

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
