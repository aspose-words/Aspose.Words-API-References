---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words لـ .NET
description: اكتشف فهرس صفحة PdfLoadOptions. اضبط فهرس صفحة البداية لقراءة ملفات PDF بسهولة باستخدام هذه الخاصية المرنة. حسّن تعاملك مع ملفات PDF اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

يحصل على أو يضبط فهرس الصفحة الأولى المراد قراءتها. القيمة الافتراضية هي 0.

```csharp
public int PageIndex { get; set; }
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
