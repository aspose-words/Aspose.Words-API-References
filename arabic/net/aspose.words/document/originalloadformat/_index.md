---
title: Document.OriginalLoadFormat
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن.
type: docs
weight: 280
url: /ar/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

الحصول على تنسيق المستند الأصلي الذي تم تحميله في هذا الكائن.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

### ملاحظات

إذا قمت بإنشاء مستند جديد فارغ ، يتم إرجاعDoc القيمة.

### أمثلة

يوضح كيفية استرداد تفاصيل عملية تحميل المستند.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### أنظر أيضا

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


