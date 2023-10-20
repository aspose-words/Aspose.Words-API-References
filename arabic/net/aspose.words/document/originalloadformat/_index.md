---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words لـ .NET
description: Document OriginalLoadFormat ملكية. الحصول على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن في C#.
type: docs
weight: 300
url: /ar/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

الحصول على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## ملاحظات

إذا قمت بإنشاء مستند فارغ جديد، فسيتم إرجاع الملفDoc قيمة.

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
