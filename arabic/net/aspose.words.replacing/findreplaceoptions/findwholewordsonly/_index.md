---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words لـ .NET
description: FindReplaceOptions FindWholeWordsOnly ملكية. يشير True إلى أن القيمة القديمة يجب أن تكون كلمة مستقلة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

يشير True إلى أن القيمة القديمة يجب أن تكون كلمة مستقلة.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## أمثلة

يوضح كيفية تبديل عمليات البحث والاستبدال المستقلة للكلمات فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "صحيح" لاستبدال النص الذي تم العثور عليه إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "خطأ" لاستبدال النص بالكامل بغض النظر عن البيئة المحيطة به.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
