---
title: FindReplaceOptions.IgnoreFootnotes
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. الحصول على قيمة منطقية أو تعيينها للإشارة إلى تجاهل الحواشي السفلية. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 90
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

الحصول على قيمة منطقية أو تعيينها للإشارة إلى تجاهل الحواشي السفلية. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

### أمثلة

يوضح كيفية تجاهل الحواشي السفلية أثناء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// اضبط علامة "IgnoreFootnotes" على "صحيح" للحصول على ميزة البحث والاستبدال
// عملية لتجاهل النص داخل الحواشي السفلية.
// اضبط علامة "IgnoreFootnotes" على "خطأ" للحصول على ميزة البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل الحواشي السفلية.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


