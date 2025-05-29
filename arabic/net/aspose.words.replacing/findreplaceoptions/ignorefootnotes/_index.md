---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FindReplaceOptions IgnoreFootnotes لإدارة الحواشي السفلية في مستنداتك بسهولة. حسّن كفاءة التحرير باستخدام هذا التبديل البسيط!
type: docs
weight: 90
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل الحواشي السفلية. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## أمثلة

يوضح كيفية تجاهل الحواشي السفلية أثناء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// اضبط علامة "IgnoreFootnotes" على "true" للحصول على خاصية البحث والاستبدال
// عملية لتجاهل النص الموجود داخل الحواشي السفلية.
// اضبط علامة "IgnoreFootnotes" على "false" للحصول على البحث والاستبدال
// عملية للبحث أيضًا عن نص داخل الحواشي السفلية.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
