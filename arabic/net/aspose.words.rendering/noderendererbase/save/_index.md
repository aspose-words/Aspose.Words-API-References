---
title: NodeRendererBase.Save
second_title: Aspose.Words لمراجع .NET API
description: NodeRendererBase طريقة. يحول الشكل إلى صورة ويحفظ في ملف.
type: docs
weight: 90
url: /ar/net/aspose.words.rendering/noderendererbase/save/
---
## Save(string, ImageSaveOptions) {#save_1}

يحول الشكل إلى صورة ويحفظ في ملف.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف الصورة. إذا كان هناك ملف بالاسم المحدد موجود بالفعل، فستتم الكتابة فوق الملف الموجود. |
| saveOptions | ImageSaveOptions | يحدد الخيارات التي تتحكم في كيفية عرض الشكل وحفظه. يمكن ان يكون`باطل`. |

### أمثلة

يوضح كيفية تقديم كائن Office Math إلى ملف صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// قم بإنشاء كائن "ImageSaveOptions" لتمريره إلى طريقة "حفظ" عارض العقدة لتعديله
// كيفية تحويل عقدة OfficeMath إلى صورة.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// اضبط خاصية "Scale" على 5 لجعل الكائن يصل إلى خمسة أضعاف حجمه الأصلي.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* مساحة الاسم [Aspose.Words.Rendering](../../noderendererbase/)
* المجسم [Aspose.Words](../../../)

---

## Save(Stream, ImageSaveOptions) {#save}

يعرض الشكل في صورة ويحفظ في دفق.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق حيث يتم حفظ صورة الشكل. |
| saveOptions | ImageSaveOptions | يحدد الخيارات التي تتحكم في كيفية عرض الشكل وحفظه. يمكن ان يكون`باطل` . إذا كان هذا`باطل`سيتم حفظ الصورة بصيغة PNG. |

### أمثلة

يوضح كيفية استخدام عارض الأشكال لتصدير الأشكال إلى الملفات الموجودة في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// يوجد 7 أشكال في المستند، بما في ذلك شكل مجموعة واحد وشكلين فرعيين.
// سنقوم بتحويل كل شكل إلى ملف صورة في نظام الملفات المحلي
// مع تجاهل أشكال المجموعة نظرًا لعدم ظهورها.
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
* مساحة الاسم [Aspose.Words.Rendering](../../noderendererbase/)
* المجسم [Aspose.Words](../../../)


