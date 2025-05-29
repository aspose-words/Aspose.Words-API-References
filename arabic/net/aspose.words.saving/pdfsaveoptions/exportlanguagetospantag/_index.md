---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ExportLanguageToSpanTag في PdfSaveOptions. تحكم في تصدير لغة النص باستخدام علامات Span لتحسين بنية المستند وسهولة الوصول إليه.
type: docs
weight: 150
url: /ar/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم إنشاء علامة "Span" في بنية المستند لتصدير لغة النص أم لا.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`ويتم ربط السمة "Lang" بتسلسل المحتوى المحدد في مجرى محتوى الصفحة.

عندما تكون القيمة`حقيقي` تم إنشاء علامة "Span" للنص الذي يحتوي على لغة غير افتراضية وتم إرفاق سمة "Lang" بهذه العلامة.

يتم تجاهل هذه القيمة عند[`ExportDocumentStructure`](../exportdocumentstructure/) يكون`خطأ شنيع` .

## أمثلة

يوضح كيفية إنشاء علامة "Span" في بنية المستند لتصدير لغة النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // ملاحظة، عندما يكون "ExportDocumentStructure" خاطئًا، سيتم تجاهل "ExportLanguageToSpanTag".
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
