---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MatchCase في FindReplaceOptions، وفعّل المقارنات الحساسة لحالة الأحرف أو غير الحساسة لها لتحرير نصوص دقيق. حسّن سير عملك!
type: docs
weight: 140
url: /ar/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

يشير True إلى مقارنة حساسة لحالة الأحرف، ويشير false إلى مقارنة غير حساسة لحالة الأحرف.

```csharp
public bool MatchCase { get; set; }
```

## أمثلة

يوضح كيفية تبديل حساسية الحالة عند إجراء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "MatchCase" على "true" لتطبيق حساسية الحالة أثناء البحث عن السلاسل التي يجب استبدالها.
// اضبط علامة "MatchCase" على "false" لتجاهل حالة الأحرف أثناء البحث عن نص لاستبداله.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
