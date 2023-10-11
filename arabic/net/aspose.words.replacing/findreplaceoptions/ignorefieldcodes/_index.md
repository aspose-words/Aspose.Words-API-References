---
title: FindReplaceOptions.IgnoreFieldCodes
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص داخل رموز الحقول. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 70
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص داخل رموز الحقول. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

### ملاحظات

يؤثر هذا الخيار على رموز الحقول فقط (لا يتجاهل العقد بين FieldSeparator وFieldEnd).

لتجاهل الحقل بأكمله، يرجى استخدام الخيار المقابل[`IgnoreFields`](../ignorefields/).

### أمثلة

يوضح كيفية تجاهل النص داخل رموز الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// استبدل "T" في المستند مع تجاهل النص الموجود داخل رمز الحقل أم لا.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


