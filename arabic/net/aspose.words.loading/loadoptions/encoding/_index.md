---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LoadOptions Encoding لإدارة ترميز مستندات HTML وTXT وCHM بسهولة. خصّص تحميل المحتوى لتحقيق أداء مثالي!
type: docs
weight: 50
url: /ar/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

يحصل على أو يعين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون`باطل` . الافتراضي هو`باطل` .

```csharp
public Encoding Encoding { get; set; }
```

## ملاحظات

يتم استخدام هذه الخاصية فقط عند تحميل مستندات HTML أو TXT أو CHM.

إذا لم يتم تحديد الترميز داخل المستند وكانت هذه الخاصية`باطل`، ثم سيحاول النظام اكتشاف الترميز تلقائيًا.

## أمثلة

يوضح كيفية تعيين الترميز الذي سيتم فتح المستند به.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// قم بتحميل المستند أثناء تمرير كائن LoadOptions، ثم تحقق من محتويات المستند.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
