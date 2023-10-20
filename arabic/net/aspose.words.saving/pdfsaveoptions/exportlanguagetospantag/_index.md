---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions ExportLanguageToSpanTag ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم إنشاء علامة Span في بنية المستند لتصدير لغة النص أم لا في C#.
type: docs
weight: 150
url: /ar/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم إنشاء علامة "Span" في بنية المستند لتصدير لغة النص أم لا.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`ويتم إرفاق السمة "Lang" بتسلسل محتوى محدد في تدفق محتوى الصفحة.

عندما تكون القيمة`حقيقي` يتم إنشاء علامة "Span" للنص الذي يحتوي على language غير الافتراضية ويتم إرفاق سمة "Lang" بهذه العلامة.

يتم تجاهل هذه القيمة عندما[`ExportDocumentStructure`](../exportdocumentstructure/) يكون`خطأ شنيع` .

## أمثلة

يوضح كيفية إنشاء علامة "Span" في بنية المستند لتصدير لغة النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // ملاحظة، عندما تكون قيمة "ExportDocumentStructure" خاطئة، يتم تجاهل "ExportLanguageToSpanTag".
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
