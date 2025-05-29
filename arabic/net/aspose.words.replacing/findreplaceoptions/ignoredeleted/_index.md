---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تجاهل المحذوفات في FindReplaceOptions، وتحكم في ظهور النص في المراجعات المحذوفة باستخدام مفتاح تبديل منطقي سهل. حسّن تجربة التحرير لديك!
type: docs
weight: 60
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل مراجعات الحذف. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## أمثلة

يوضح كيفية تضمين النص أو تجاهله داخل مراجعات الحذف أثناء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// ابدأ بتتبع المراجعات وقم بإزالة الفقرة الثانية، مما سيؤدي إلى إنشاء مراجعة حذف.
// سوف تظل هذه الفقرة موجودة في المستند حتى نقبل تعديل الحذف.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreDeleted" على "true" للحصول على خاصية البحث والاستبدال
// عملية لتجاهل الفقرات التي تحتوي على مراجعات حذف.
// اضبط علامة "IgnoreDeleted" على "false" للحصول على البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل المراجعات المحذوفة.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
