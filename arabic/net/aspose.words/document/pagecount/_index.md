---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Document PageCount، التي تكشف عن إجمالي عدد الصفحات استنادًا إلى أحدث تخطيط، مما يضمن إدارة المستندات والرؤى الدقيقة.
type: docs
weight: 330
url: /ar/net/aspose.words/document/pagecount/
---
## Document.PageCount property

يحصل على عدد الصفحات في المستند كما تم حسابه بواسطة عملية تخطيط الصفحة الأخيرة.

```csharp
public int PageCount { get; }
```

## أمثلة

يوضح كيفية حساب عدد الصفحات في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

//التحقق من عدد الصفحات المتوقعة للمستند.
Assert.AreEqual(3, doc.PageCount);

// الحصول على خاصية PageCount استدعى تخطيط صفحة المستند لحساب القيمة.
// لن تكون هناك حاجة إلى إعادة تنفيذ هذه العملية عند عرض المستند بتنسيق حفظ الصفحة الثابتة،
// مثل .pdf. هذا يوفر عليك الوقت، خاصةً مع المستندات الأكثر تعقيدًا.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### أنظر أيضا

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
