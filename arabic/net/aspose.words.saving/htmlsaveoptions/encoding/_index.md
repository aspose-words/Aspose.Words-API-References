---
title: Encoding
second_title: Aspose.Words لمراجع .NET API
description: يحدد الترميز المراد استخدامه عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيترميز UTF8 جديد خطأ UTF-8 بدون BOM .
type: docs
weight: 100
url: /ar/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

يحدد الترميز المراد استخدامه عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`ترميز UTF8 جديد (خطأ)` (UTF-8 بدون BOM) .

```csharp
public Encoding Encoding { get; set; }
```

### أمثلة

يوضح كيفية استخدام ترميز معين عند حفظ مستند في epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// استخدم كائن SaveOptions لتحديد ترميز المستند الذي سنقوم بحفظه.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// بشكل افتراضي ، سيكون لمستند الإخراج .epub جميع محتوياته في جزء HTML واحد.
// يسمح لنا معيار الانقسام بتقسيم المستند إلى عدة أجزاء بتنسيق HTML.
// سنضع المعايير لتقسيم الوثيقة إلى فقرات عنوان.
// هذا مفيد للقراء الذين لا يستطيعون قراءة ملفات HTML أكثر من حجم معين.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// حدد أننا نريد تصدير خصائص المستند.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### أنظر أيضا

* class [HtmlSaveOptions](../../htmlsaveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
