---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تتيح لك خاصية MarkdownSaveOptions ExportAsHtml تخصيص عناصر HTML لتصدير Markdown بسلاسة. حسّن تنوع محتواك إلى أقصى حد!
type: docs
weight: 30
url: /ar/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown بصيغة HTML خام. القيمة الافتراضية هيNone .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

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

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
