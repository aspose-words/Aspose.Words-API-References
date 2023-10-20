---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words لـ .NET
description: FindReplaceOptions IgnoreFields ملكية. الحصول على قيمة منطقية أو تعيينها للإشارة إلى تجاهل النص الموجود داخل الحقول. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

الحصول على قيمة منطقية أو تعيينها للإشارة إلى تجاهل النص الموجود داخل الحقول. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreFields { get; set; }
```

## ملاحظات

يؤثر هذا الخيار على الحقل بأكمله (جميع العقد بين FieldStart وFieldEnd).

لتجاهل رموز الحقول فقط، يرجى استخدام الخيار المقابل[`IgnoreFieldCodes`](../ignorefieldcodes/).

## أمثلة

يوضح كيفية تجاهل النص داخل الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreFields" على "صحيح" للحصول على عملية البحث والاستبدال
// عملية لتجاهل النص داخل الحقول.
// اضبط علامة "IgnoreFields" على "خطأ" للحصول على عملية البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل الحقول.
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
