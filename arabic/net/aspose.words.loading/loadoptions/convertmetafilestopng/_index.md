---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words لـ .NET
description: حوّل ملفات WMF وEMF إلى صيغة PNG بسهولة مع LoadOptions. بسّط إدارة صورك وحسّن توافقها اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

يحصل على أو يحدد ما إذا كان سيتم تحويل الملف التعريفي (Wmf أوEmf ) الصور إلىPngتنسيق الصورة.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## ملاحظات

ملفات التعريف (Wmf أوEmf ) هو تنسيق صورة غير مضغوط ويتطلب في بعض الأحيان قدرًا كبيرًا من ذاكرة الوصول العشوائي (RAM) لحفظ ومعالجة المستند. يسمح هذا الخيار بتحويل جميع صور الملفات التعريفية إلىPng عند تحميل المستند. يرجى ملاحظة - تحويل الرسومات المتجهة إلى رسومات نقطية يقلل من جودة الصور.

## أمثلة

يوضح كيفية تحويل WMF/EMF إلى PNG أثناء تحميل المستند.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.CreateImageDirectly.docx");

shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

TestUtil.VerifyImageInShape(1600, 1600, ImageType.Wmf, shape);

LoadOptions loadOptions = new LoadOptions();
loadOptions.ConvertMetafilesToPng = true;

doc = new Document(ArtifactsDir + "Image.CreateImageDirectly.docx", loadOptions);
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
