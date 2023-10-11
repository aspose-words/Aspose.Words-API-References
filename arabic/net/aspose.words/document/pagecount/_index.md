---
title: Document.PageCount
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على عدد الصفحات في المستند كما تم حسابه بواسطة عملية تخطيط الصفحة الأخيرة.
type: docs
weight: 320
url: /ar/net/aspose.words/document/pagecount/
---
## Document.PageCount property

الحصول على عدد الصفحات في المستند كما تم حسابه بواسطة عملية تخطيط الصفحة الأخيرة.

```csharp
public int PageCount { get; }
```

### أمثلة

يوضح كيفية حساب عدد الصفحات في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// التحقق من عدد الصفحات المتوقع للمستند.
Assert.AreEqual(3, doc.PageCount);

// يؤدي الحصول على خاصية PageCount إلى استدعاء تخطيط صفحة المستند لحساب القيمة.
// لن يلزم إعادة تنفيذ هذه العملية عند عرض المستند بتنسيق حفظ صفحة ثابت،
// مثل .pdf. لذا يمكنك توفير بعض الوقت، خاصة مع المستندات الأكثر تعقيدًا.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### أنظر أيضا

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


