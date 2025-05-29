---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FindReplaceOptions IgnoreFields لإدارة النصوص داخل الحقول بسهولة. تحكّم في وقت تجاهل المحتوى لضمان بحث فعّال!
type: docs
weight: 80
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل الحقول. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreFields { get; set; }
```

## ملاحظات

يؤثر هذا الخيار على الحقل بأكمله (كل العقد بين FieldStart وFieldEnd).

لتجاهل رموز الحقول فقط، يرجى استخدام الخيار المقابل[`IgnoreFieldCodes`](../ignorefieldcodes/).

## أمثلة

يوضح كيفية تجاهل النص الموجود داخل الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreFields" على "true" للحصول على البحث والاستبدال
// عملية تجاهل النص الموجود داخل الحقول.
// اضبط علامة "IgnoreFields" على "false" للحصول على البحث والاستبدال
// عملية للبحث أيضًا عن النص داخل الحقول.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
