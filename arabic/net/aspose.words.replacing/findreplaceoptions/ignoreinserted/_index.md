---
title: FindReplaceOptions.IgnoreInserted
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل مراجعات الإدراج . القيمة الافتراضية هيخاطئة .
type: docs
weight: 100
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

الحصول على أو تعيين قيمة منطقية تشير إما إلى تجاهل النص داخل مراجعات الإدراج . القيمة الافتراضية هي`خاطئة` .

```csharp
public bool IgnoreInserted { get; set; }
```

### أمثلة

يوضح كيفية تضمين أو تجاهل النص داخل إدراج المراجعات أثناء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// بدء تتبع المراجعات وإدراج فقرة. ستكون تلك الفقرة عبارة عن إدخال تنقيح.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreInserted" على "true" للحصول على البحث والاستبدال
// لتجاهل الفقرات التي تحتوي على مراجعات.
// اضبط علامة "IgnoreInserted" على "false" للحصول على البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل إدخال المراجعات.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


