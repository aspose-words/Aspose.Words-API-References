---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FindWholeWordsOnly على تعزيز بحثك بنتائج دقيقة، مما يضمن تطابق oldValue فقط ككلمة مستقلة.
type: docs
weight: 50
url: /ar/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

يشير True إلى أن oldValue يجب أن تكون كلمة مستقلة.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## أمثلة

يوضح كيفية تبديل عمليات البحث والاستبدال الخاصة بالكلمات المستقلة فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "true" لاستبدال النص الموجود إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "false" لاستبدال كل النص بغض النظر عن محيطه.
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
