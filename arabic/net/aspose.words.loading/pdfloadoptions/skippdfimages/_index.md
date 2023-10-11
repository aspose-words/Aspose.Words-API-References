---
title: PdfLoadOptions.SkipPdfImages
second_title: Aspose.Words لمراجع .NET API
description: PdfLoadOptions ملكية. الحصول على أو تعيين العلامة التي تشير إلى ما إذا كان يجب تخطي الصور أثناء تحميل مستند PDF. الافتراضي هوخطأ شنيع .
type: docs
weight: 40
url: /ar/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

الحصول على أو تعيين العلامة التي تشير إلى ما إذا كان يجب تخطي الصور أثناء تحميل مستند PDF. الافتراضي هو`خطأ شنيع` .

```csharp
public bool SkipPdfImages { get; set; }
```

### أمثلة

يوضح كيفية تخطي الصور أثناء تحميل ملفات PDF.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
{
    Assert.AreEqual(shapeCollection.Count, 0);
}
else
{
    Assert.AreNotEqual(shapeCollection.Count, 0);
}
```

### أنظر أيضا

* class [PdfLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../pdfloadoptions/)
* المجسم [Aspose.Words](../../../)


