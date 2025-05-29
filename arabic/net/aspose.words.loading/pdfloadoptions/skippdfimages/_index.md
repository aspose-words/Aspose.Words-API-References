---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SkipPdfImages في PdfLoadOptions للتحكم في تحميل الصور في ملفات PDF. حسّن الأداء بتخطي الصور لمعالجة أسرع للمستندات.
type: docs
weight: 40
url: /ar/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

يحصل على أو يضبط العلامة التي تشير إلى ضرورة تخطي الصور أثناء تحميل مستند PDF. الإعداد الافتراضي هو`خطأ شنيع` .

```csharp
public bool SkipPdfImages { get; set; }
```

## أمثلة

يوضح كيفية تخطي الصور أثناء تحميل ملفات PDF.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### أنظر أيضا

* class [PdfLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
