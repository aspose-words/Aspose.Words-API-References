---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FindReplaceOptions IgnoreFieldCodes لإدارة النصوص في رموز الحقول بسهولة. تحكم في الرؤية بإعداد منطقي بسيط!
type: docs
weight: 70
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل أكواد الحقول. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## ملاحظات

يؤثر هذا الخيار على أكواد الحقول فقط (لا يتجاهل العقد بين FieldSeparator وFieldEnd).

لتجاهل الحقل بأكمله، يرجى استخدام الخيار المقابل[`IgnoreFields`](../ignorefields/).

## أمثلة

يوضح كيفية تجاهل النص الموجود داخل رموز الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// استبدال 'T' في المستند بتجاهل النص الموجود داخل رمز الحقل أم لا.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
