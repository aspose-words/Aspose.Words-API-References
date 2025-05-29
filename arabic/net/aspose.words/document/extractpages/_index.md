---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Document ExtractPages لاسترداد نطاقات صفحات محددة بسهولة، مما يعزز إدارة المستندات لديك وكفاءتها.
type: docs
weight: 640
url: /ar/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

يعيد[`Document`](../) كائن يمثل نطاقًا محددًا من الصفحات.

```csharp
public Document ExtractPages(int index, int count)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس المبني على الصفر للصفحة الأولى التي سيتم استخراجها. |
| count | Int32 | عدد الصفحات المطلوب استخراجها. |

## ملاحظات

يجب أن تبدو الوثيقة الناتجة مثل تلك الموجودة في MS Word، كما لو كنا قد قمنا بطباعة صفحات محددة - سيتم الحفاظ على الترقيم، ورؤوس الصفحات/تذييلاتها وتخطيط الجداول المتقاطعة. ولكن بسبب وجود عدد كبير من الفروق الدقيقة، التي تظهر أثناء تقليل عدد الصفحات، فإن التطابق الكامل للتخطيط هو مهمة معقدة للغاية تتطلب الكثير من الجهد. اعتمادًا على تعقيد الوثيقة، قد تكون هناك اختلافات طفيفة في تخطيط محتويات الوثيقة الناتجة مقارنة بالوثيقة المصدر. سيكون موضع تقدير كبير أي ملاحظات.

## أمثلة

يوضح كيفية الحصول على نطاق محدد من الصفحات من المستند.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
