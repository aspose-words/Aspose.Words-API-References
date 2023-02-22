---
title: LoadOptions.Encoding
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions ملكية. الحصول على أو تعيين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون فارغًا. الافتراضي هو فارغ.
type: docs
weight: 50
url: /ar/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

الحصول على أو تعيين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون فارغًا. الافتراضي هو فارغ.

```csharp
public Encoding Encoding { get; set; }
```

### ملاحظات

تُستخدم هذه الخاصية فقط عند تحميل مستندات HTML أو TXT أو CHM.

إذا لم يتم تحديد الترميز داخل المستند وكانت هذه الخاصية`لا شيء`، ثم سيحاول النظام اكتشاف الترميز تلقائيًا.

### أمثلة

يوضح كيفية ضبط الترميز الذي يتم فتح المستند به.

```csharp
// سيكتشف كائن FileFormatInfo هذا الملف على أنه تم ترميزه في شيء آخر غير UTF-7.
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Encoded in UTF-7.txt");

Assert.AreNotEqual(Encoding.UTF7, fileFormatInfo.Encoding);

// إذا قمنا بتحميل المستند بدون أي تكوينات تحميل ، فستكتشف Aspose.Words ترميزه كـ UTF-8.
Document doc = new Document(MyDir + "Encoded in UTF-7.txt");

// المحتويات ، المحللة في UTF-8 ، تنشئ سلسلة صالحة.
// ومع ذلك ، مع العلم أن الملف بتنسيق UTF-7 ، يمكننا أن نرى أن النتيجة غير صحيحة.
Assert.AreEqual("Hello world+ACE-", doc.ToString(SaveFormat.Text).Trim());

// في حالات الترميز الغامض مثل هذا ، يمكننا تعيين متغير ترميز محدد
// لتحليل الملف داخل كائن LoadOptions.
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.UTF7
};

// قم بتحميل المستند أثناء تمرير كائن LoadOptions ، ثم تحقق من محتويات المستند.
doc = new Document(MyDir + "Encoded in UTF-7.txt", loadOptions);

Assert.AreEqual("Hello world!", doc.ToString(SaveFormat.Text).Trim());
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


