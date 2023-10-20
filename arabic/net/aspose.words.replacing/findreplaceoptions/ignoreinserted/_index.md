---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words لـ .NET
description: FindReplaceOptions IgnoreInserted ملكية. الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص الموجود داخل مراجعات الإدراج. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص الموجود داخل مراجعات الإدراج. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreInserted { get; set; }
```

## أمثلة

يوضح كيفية تضمين النص أو تجاهله داخل مراجعات الإدراج أثناء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// ابدأ بتتبع المراجعات وأدخل فقرة. ستكون هذه الفقرة عبارة عن مراجعة إدراج.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreInserted" على "صحيح" للحصول على عملية البحث والاستبدال
// عملية لتجاهل الفقرات التي يتم إدراج المراجعات فيها.
// اضبط علامة "IgnoreInserted" على "خطأ" للحصول على عملية البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل إدراج المراجعات.
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
