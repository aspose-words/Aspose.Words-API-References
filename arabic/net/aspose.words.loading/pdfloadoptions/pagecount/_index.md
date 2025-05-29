---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words لـ .NET
description: تحكم في قراءة الصفحات باستخدام خاصية PageCount في PdfLoadOptions. حدّد بسهولة عدد الصفحات المراد قراءتها، مما يضمن معالجة فعّالة للمستندات.
type: docs
weight: 20
url: /ar/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

يُحدِّد أو يُحدِّد عدد الصفحات المراد قراءتها. القيمة الافتراضية هي MaxValue، مما يعني أنه سيتم قراءة جميع صفحات المستند.

```csharp
public int PageCount { get; set; }
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
