---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OriginalLoadFormat للوصول بسهولة إلى تنسيق المستند الأصلي المحمّل في الكائن الخاص بك، مما يؤدي إلى تحسين إدارة المستندات.
type: docs
weight: 310
url: /ar/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

يحصل على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## ملاحظات

إذا قمت بإنشاء مستند فارغ جديد، فسيتم إرجاعDoc قيمة.

## أمثلة

يوضح كيفية استرداد تفاصيل عملية تحميل المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### أنظر أيضا

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
