---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words لـ .NET
description: FindReplaceOptions IgnoreDeleted ملكية. الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص داخل حذف المراجعات. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

الحصول على قيمة منطقية أو تعيينها تشير إما إلى تجاهل النص داخل حذف المراجعات. القيمة الافتراضية هي`خطأ شنيع` .

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

// ابدأ في تتبع المراجعات وقم بإزالة الفقرة الثانية التي ستؤدي إلى إنشاء مراجعة حذف.
// ستظل هذه الفقرة موجودة في المستند حتى نقبل مراجعة الحذف.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "IgnoreDeleted" على "صحيح" للحصول على عملية البحث والاستبدال
// عملية لتجاهل الفقرات التي تحذف المراجعات.
// اضبط علامة "IgnoreDeleted" على "خطأ" للحصول على عملية البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل حذف المراجعات.
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
