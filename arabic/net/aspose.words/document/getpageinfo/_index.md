---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetPageInfo لاسترداد حجم الصفحة الأساسي والاتجاه وتفاصيل العرض لتحسين الطباعة وإدارة المستندات.
type: docs
weight: 650
url: /ar/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

يحصل على حجم الصفحة والاتجاه ومعلومات أخرى حول الصفحة التي قد تكون مفيدة للطباعة أو العرض.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pageIndex | Int32 | فهرس الصفحة المبني على 0. |

## أمثلة

يوضح كيفية التحقق مما إذا كانت الصفحة ملونة أم لا.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// تأكد من أن الصفحة الأولى من المستند ليست ملونة.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### أنظر أيضا

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
