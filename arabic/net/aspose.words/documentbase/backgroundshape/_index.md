---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words لـ .NET
description: DocumentBase BackgroundShape ملكية. الحصول على شكل خلفية المستند أو تعيينه. يمكن ان يكونباطل  في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

الحصول على شكل خلفية المستند أو تعيينه. يمكن ان يكون`باطل` .

```csharp
public Shape BackgroundShape { get; set; }
```

## ملاحظات

يسمح Microsoft Word فقط بالشكل الذي له خاصيته[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) الخاصيةتساوي لRectangle لاستخدامها كشكل خلفية للمستند.

يدعم Microsoft Word خصائص التعبئة لشكل الخلفية فقط. يتم تجاهل كافة خصائص الأخرى.

سيؤدي تعيين هذه الخاصية إلى قيمة غير فارغة إلى تعيين القيمة أيضًا[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) ل`حقيقي`.

## أمثلة

يوضح كيفية تعيين شكل خلفية لكل صفحة من المستند.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// نوع الشكل الوحيد الذي يمكننا استخدامه كخلفية هو المستطيل.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// هناك طريقتان لاستخدام هذا الشكل كخلفية للصفحة.
// 1 - لون مسطح:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - صورة:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// اضبط مظهر الصورة لجعلها أكثر ملاءمة كعلامة مائية.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word لا يدعم الأشكال التي تحتوي على صور كخلفيات،
// ولكن لا يزال بإمكاننا رؤية هذه الخلفيات بتنسيقات حفظ أخرى مثل ‎.pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
