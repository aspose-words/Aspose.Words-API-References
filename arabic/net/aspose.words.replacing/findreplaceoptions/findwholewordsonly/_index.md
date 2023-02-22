---
title: FindReplaceOptions.FindWholeWordsOnly
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. صحيح يشير إلى أن oldValue يجب أن تكون كلمة قائمة بذاتها.
type: docs
weight: 50
url: /ar/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

صحيح يشير إلى أن oldValue يجب أن تكون كلمة قائمة بذاتها.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

### أمثلة

يوضح كيفية التبديل بين عمليات البحث والاستبدال المستقلة عن الكلمات فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "true" لاستبدال النص الذي تم العثور عليه إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "خطأ" لاستبدال كل النص بغض النظر عن ما يحيط به.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


