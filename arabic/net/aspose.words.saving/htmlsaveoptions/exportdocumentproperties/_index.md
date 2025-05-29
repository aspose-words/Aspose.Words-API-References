---
title: HtmlSaveOptions.ExportDocumentProperties
linktitle: ExportDocumentProperties
articleTitle: ExportDocumentProperties
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل ExportDocumentProperties في HtmlSaveOptions على تعزيز صادراتك بتنسيق HTML أو MHTML أو EPUB من خلال تضمين خصائص المستندات المخصصة والمضمنة الأساسية.
type: docs
weight: 120
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

يحدد ما إذا كان سيتم تصدير خصائص المستند المضمنة والمخصصة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

## أمثلة

يوضح كيفية استخدام ترميز معين عند حفظ مستند بتنسيق .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// استخدم كائن SaveOptions لتحديد الترميز للمستند الذي سنحفظه.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// بشكل افتراضي، سيكون مستند .epub الناتج يحتوي على كل محتوياته في جزء HTML واحد.
// يسمح لنا معيار التقسيم بتقسيم المستند إلى عدة أجزاء HTML.
// سوف نقوم بتحديد المعايير لتقسيم المستند إلى فقرات عنوانية.
// يعد هذا مفيدًا للقراء الذين لا يستطيعون قراءة ملفات HTML ذات حجم أكبر من حجم معين.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// حدد أننا نريد تصدير خصائص المستند.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
