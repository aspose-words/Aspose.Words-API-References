---
title: RtfSaveOptions.SaveImagesAsWmf
second_title: Aspose.Words لمراجع .NET API
description: RtfSaveOptions ملكية. متىحقيقي سيتم حفظ جميع الصور بتنسيق WMF.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

متى`حقيقي` سيتم حفظ جميع الصور بتنسيق WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

### ملاحظات

قد يساعد هذا الخيار في تجنب رسائل تحذير الدفتر.

### أمثلة

يوضح كيفية تحويل جميع الصور في مستند إلى تنسيق Windows Metafile حيث نقوم بحفظ المستند بتنسيق RTF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.AreEqual(ImageType.Jpeg, imageShape.ImageData.ImageType);

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ImageType.Png, imageShape.ImageData.ImageType);

// قم بإنشاء كائن "RtfSaveOptions" لتمريره إلى طريقة "حفظ" المستند لتعديل كيفية حفظه في RTF.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// قم بتعيين خاصية "SaveImagesAsWmf" على "true" لتحويل جميع الصور الموجودة في المستند إلى WMF أثناء حفظها في RTF.
// القيام بذلك سيساعد القراء مثل الدفتر على قراءة وثيقتنا.
// اضبط الخاصية "SaveImagesAsWmf" على "خطأ" للحفاظ على التنسيق الأصلي لجميع الصور في المستند
// كما نحفظه في RTF. سيؤدي هذا إلى الحفاظ على جودة الصور على حساب التوافق مع أجهزة قراءة RTF الأقدم.
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[1]).ImageData.ImageType);
}
else
{
    Assert.AreEqual(ImageType.Jpeg, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Png, ((Shape)shapes[1]).ImageData.ImageType);
}
```

### أنظر أيضا

* class [RtfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../rtfsaveoptions/)
* المجسم [Aspose.Words](../../../)


