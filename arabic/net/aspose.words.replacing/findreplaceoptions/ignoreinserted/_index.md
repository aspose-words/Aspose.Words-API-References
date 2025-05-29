---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FindReplaceOptions IgnoreInserted، وتحكم في معالجة النصوص في مراجعات الإدراج باستخدام هذا الإعداد المنطقي البسيط. القيمة الافتراضية هي False.
type: docs
weight: 100
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل النص داخل مراجعات الإدراج. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreInserted { get; set; }
```

## أمثلة

يوضح كيفية تضمين النص أو تجاهله داخل مراجعات الإدراج أثناء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// ابدأ بتتبع المراجعات وأدرج فقرة. ستكون هذه الفقرة مراجعة إدراج.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreInserted" على "true" للحصول على البحث والاستبدال
// عملية لتجاهل الفقرات التي تحتوي على مراجعات إدراجية.
// اضبط علامة "IgnoreInserted" على "false" للحصول على البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل المراجعات المدرجة.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
