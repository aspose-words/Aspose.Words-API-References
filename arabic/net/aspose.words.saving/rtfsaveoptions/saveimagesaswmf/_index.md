---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية RtfSaveOptions SaveImagesAsWmf على تعزيز مستندك عن طريق حفظ كافة الصور بتنسيق WMF لتحقيق جودة وتوافق فائقين.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

عندما`حقيقي` سيتم حفظ جميع الصور بتنسيق WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## ملاحظات

قد يساعد هذا الخيار في تجنب رسائل تحذير WordPad.

## أمثلة

يوضح كيفية تحويل كافة الصور في مستند إلى تنسيق Windows Metafile أثناء حفظ المستند بتنسيق RTF.

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

// قم بضبط الخاصية "SaveImagesAsWmf" على "true" لتحويل كافة الصور في المستند إلى WMF أثناء حفظه في RTF.
// إن القيام بذلك سيساعد القراء مثل WordPad على قراءة مستندنا.
// اضبط خاصية "SaveImagesAsWmf" على "false" للحفاظ على التنسيق الأصلي لجميع الصور في المستند
// عند حفظها بتنسيق RTF، سيحافظ هذا على جودة الصور على حساب التوافق مع قارئات RTF القديمة.
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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
