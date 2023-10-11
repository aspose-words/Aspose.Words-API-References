---
title: LoadOptions.Encoding
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions ملكية. الحصول على أو تعيين التشفير الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد التشفير داخل المستند. يمكن أن يكونباطل . الافتراضي هوباطل .
type: docs
weight: 50
url: /ar/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

الحصول على أو تعيين التشفير الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد التشفير داخل المستند. يمكن أن يكون`باطل` . الافتراضي هو`باطل` .

```csharp
public Encoding Encoding { get; set; }
```

### ملاحظات

تُستخدم هذه الخاصية فقط عند تحميل مستندات HTML أو TXT أو CHM.

إذا لم يتم تحديد الترميز داخل المستند وكانت هذه الخاصية`باطل`، فسيحاول النظام اكتشاف التشفير تلقائيًا .

### أمثلة

يوضح كيفية ضبط الترميز الذي سيتم من خلاله فتح المستند.

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
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


