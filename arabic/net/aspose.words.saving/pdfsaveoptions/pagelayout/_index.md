---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PdfSaveOptions PageLayout لتخصيص تخطيط ملف PDF لعرض مثالي على أي قارئ. حسّن عرض مستندك!
type: docs
weight: 250
url: /ar/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

يحدد تخطيط الصفحة الذي سيتم استخدامه عند فتح المستند في قارئ PDF.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## ملاحظات

القيمة الافتراضية هيSinglePage .

## أمثلة

يوضح كيفية عرض الصفحات عند فتحها في قارئ PDF.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// عرض الصفحات صفحتين في كل مرة، مع وضع الصفحات ذات الأرقام الفردية على اليسار.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### أنظر أيضا

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
