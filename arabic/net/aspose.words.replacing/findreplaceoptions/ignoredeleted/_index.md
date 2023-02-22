---
title: FindReplaceOptions.IgnoreDeleted
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل مراجعات حذف . القيمة الافتراضية هيخاطئة .
type: docs
weight: 60
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل مراجعات حذف . القيمة الافتراضية هي`خاطئة` .

```csharp
public bool IgnoreDeleted { get; set; }
```

### أمثلة

يوضح كيفية تضمين نص أو تجاهله داخل مراجعات الحذف أثناء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// بدء تتبع المراجعات وإزالة الفقرة الثانية ، والتي ستنشئ مراجعة حذف.
// ستستمر هذه الفقرة في المستند حتى نقبل مراجعة الحذف.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreDeleted" على "true" للحصول على البحث والاستبدال
// لتجاهل الفقرات التي تمثل حذف المراجعات.
// اضبط علامة "IgnoreDeleted" على "false" للحصول على البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل مراجعات الحذف.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


