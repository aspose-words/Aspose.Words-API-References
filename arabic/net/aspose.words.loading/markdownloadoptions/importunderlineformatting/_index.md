---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MarkdownLoadOptions ImportUnderlineFormatting. تحكّم بتنسيق النص المسطر باستخدام إعداد منطقي بسيط. حسّن تجربة Markdown الخاصة بك!
type: docs
weight: 20
url: /ar/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

يحصل على قيمة منطقية أو يعينها للإشارة إلى التعرف على تسلسل مكون من حرفين زائد "++" كتنسيق نص مسطر. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## أمثلة

يوضح كيفية التعرف على أحرف الجمع "++" كتنسيق نص مسطر.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### أنظر أيضا

* class [MarkdownLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
