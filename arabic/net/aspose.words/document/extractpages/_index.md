---
title: Document.ExtractPages
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. إرجاعDocument كائن يمثل نطاقًا محددًا من الصفحات.
type: docs
weight: 620
url: /ar/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

إرجاع[`Document`](../) كائن يمثل نطاقًا محددًا من الصفحات.

```csharp
public Document ExtractPages(int index, int count)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس الصفري للصفحة الأولى المراد استخراجها. |
| count | Int32 | عدد الصفحات المراد استخراجها. |

### ملاحظات

يجب أن يبدو المستند الناتج مثل المستند الموجود في برنامج MS Word، كما لو أننا قمنا بطباعة صفحات محددة - سيتم الحفاظ على الترقيم، وتخطيط الرؤوس/التذييلات والجداول المتقاطعة. ولكن بسبب العدد الكبير من الفروق الدقيقة، التي تظهر مع تقليل عدد الصفحات، تعد المطابقة الكاملة للتخطيط مهمة معقدة للغاية تتطلب الكثير من الجهد. اعتمادًا على مدى تعقيد المستند، قد تكون هناك اختلافات طفيفة في تخطيط محتويات المستند الناتج مقارنة بالمستند المصدر. أي تعليقات ستكون مفيدة يكون موضع تقدير كبير.

### أمثلة

يوضح كيفية الحصول على نطاق محدد من الصفحات من المستند.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


