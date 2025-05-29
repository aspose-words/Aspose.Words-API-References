---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية شكل الخلفية في DocumentBase، وخصّص شكل خلفية مستندك بسهولة لتحسين مظهره. حسّن تصميمك إلى أقصى حد!
type: docs
weight: 10
url: /ar/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

يحصل على شكل خلفية المستند أو يضبطه. يمكن استخدامه`باطل` .

```csharp
public Shape BackgroundShape { get; set; }
```

## ملاحظات

يسمح Microsoft Word فقط بالشكل الذي يحتوي على[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) الخاصية تساوي إلىRectangle لاستخدامها كشكل خلفية للمستند.

يدعم Microsoft Word خصائص التعبئة لشكل الخلفية فقط. يتم تجاهل جميع الخصائص الأخرى.

سيؤدي تعيين هذه الخاصية إلى قيمة غير فارغة أيضًا إلى تعيين[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) ل`حقيقي`.

## أمثلة

يوضح كيفية تعيين شكل الخلفية لكل صفحة من المستند.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

//نوع الشكل الوحيد الذي يمكننا استخدامه كخلفية هو المستطيل.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// هناك طريقتان لاستخدام هذا الشكل كخلفية للصفحة.
// 1 - لون مسطح:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - صورة:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

//ضبط مظهر الصورة لجعلها أكثر ملاءمة كعلامة مائية.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// لا يدعم Microsoft Word الأشكال التي تحتوي على صور كخلفيات،
// ولكن لا يزال بإمكاننا رؤية هذه الخلفيات بتنسيقات حفظ أخرى مثل .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
