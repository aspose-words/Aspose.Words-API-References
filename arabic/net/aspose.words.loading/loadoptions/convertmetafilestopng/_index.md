---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words لـ .NET
description: LoadOptions ConvertMetafilesToPng ملكية. يحصل على أو يحدد ما إذا كان سيتم تحويل ملف التعريف Wmf أوEmf  الصور لPng تنسيق الصورة في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

يحصل على أو يحدد ما إذا كان سيتم تحويل ملف التعريف (Wmf أوEmf ) الصور لPng تنسيق الصورة.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## ملاحظات

ملفات التعريف (Wmf أوEmf ) هو تنسيق صورة غير مضغوط ويتطلب أحيانًا قدرًا كبيرًا من ذاكرة الوصول العشوائي للاحتفاظ بالمستند ومعالجته. يسمح هذا الخيار بتحويل جميع صور ملفات التعريف إلىPng عند تحميل المستند. يرجى ملاحظة أن تحويل الرسومات المتجهة إلى خطوط نقطية يقلل من جودة الصور.

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

#if NET48
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#elif NET5_0_OR_GREATER
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#endif
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
