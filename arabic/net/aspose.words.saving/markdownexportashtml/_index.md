---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Saving.MarkdownExportAsHtml enum لتحويل عناصر Markdown إلى HTML خام بسهولة، مما يعزز خيارات تصدير المستندات لديك.
type: docs
weight: 6020
url: /ar/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown بصيغة HTML خام.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | تصدير جميع العناصر باستخدام صيغة Markdown دون أي HTML خام. |
| Tables | `1` | تصدير الجداول بصيغة HTML الخام. |

## أمثلة

يوضح كيفية تصدير جدول إلى Markdown بصيغة HTML الخام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

//إنشاء جدول.
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
