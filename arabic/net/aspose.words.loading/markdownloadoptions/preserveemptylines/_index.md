---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية MarkdownLoadOptions PreserveEmptyLines على تعزيز تحميل مستند Markdown الخاص بك عن طريق الحفاظ على الأسطر الفارغة لتحسين إمكانية القراءة.
type: docs
weight: 30
url: /ar/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم الاحتفاظ بالأسطر الفارغة أثناء تحميلMarkdown document. القيمة الافتراضية هي`خطأ شنيع` .

عادةً، يتم تجاهل الأسطر الفارغة بين عناصر مستوى الكتلة في Markdown. كما يتم تجاهل الأسطر الفارغة في بداية ونهاية المستند. يسمح هذا الخيار باستيراد هذه الأسطر الفارغة.

```csharp
public bool PreserveEmptyLines { get; set; }
```

## أمثلة

يوضح كيفية الحفاظ على السطر الفارغ أثناء تحميل المستند.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### أنظر أيضا

* class [MarkdownLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
