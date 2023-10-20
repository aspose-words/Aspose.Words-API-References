---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words لـ .NET
description: FindReplaceOptions MatchCase ملكية. يشير True إلى مقارنة حساسة لحالة الأحرف ويشير false إلى مقارنة حساسة لحالة الأحرف في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

يشير True إلى مقارنة حساسة لحالة الأحرف، ويشير false إلى مقارنة حساسة لحالة الأحرف.

```csharp
public bool MatchCase { get; set; }
```

## أمثلة

يوضح كيفية تبديل حساسية حالة الأحرف عند إجراء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "MatchCase" على "صحيح" لتطبيق حساسية حالة الأحرف أثناء البحث عن سلاسل لاستبدالها.
// اضبط علامة "MatchCase" على "خطأ" لتجاهل حالة الأحرف أثناء البحث عن نص لاستبداله.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
