---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية MarkdownSaveOptions ExportUnderlineFormatting تصدير نصك. تحكّم بسهولة في تنسيق التسطير باستخدام هذا الإعداد المنطقي.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تصدير تنسيق نص underline كتسلسل من حرفين زائد "++". القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## أمثلة

يوضح كيفية تصدير تنسيق التسطير بصيغة ++.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### أنظر أيضا

* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
