---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words لـ .NET
description: استكشف خصائص DocumentBase لإدارة مستنداتك بكفاءة. تمتع بسهولة الوصول وحسّن سير عملك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

يحصل على هذه المثيل.

```csharp
public override DocumentBase Document { get; }
```

## أمثلة

يوضح كيفية إنشاء مستند بسيط.

```csharp
Document doc = new Document();

// تأتي كائنات المستند الجديد بشكل افتراضي مع الحد الأدنى من مجموعة العقد
// مطلوب لبدء إضافة محتوى مثل النص والأشكال: قسم، ونص، وفقرة.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
