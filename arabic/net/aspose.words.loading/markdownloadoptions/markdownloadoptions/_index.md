---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ MarkdownLoadOptions لتهيئة مثيلات MarkdownLoadOptions بسهولة لتحسين معالجة المستندات والتخصيص.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

يقوم بتهيئة مثيل جديد لـ[`MarkdownLoadOptions`](../) الصف.

```csharp
public MarkdownLoadOptions()
```

## ملاحظات

يتم التعيين تلقائيًا[`LoadFormat`](../../../aspose.words/loadformat/) لMarkdown .

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
