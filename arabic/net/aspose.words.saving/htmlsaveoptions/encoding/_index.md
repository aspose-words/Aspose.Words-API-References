---
title: HtmlSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words لـ .NET
description: اكتشف ترميز HtmlSaveOptions لتصدير ملفات HTML وMHTML وEPUB بسلاسة. خصص الترميز بسهولة باستخدام UTF-8 لتحقيق توافق وأداء مثاليين.
type: docs
weight: 100
url: /ar/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

يحدد الترميز الذي سيتم استخدامه عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`ترميز UTF8 الجديد (خطأ)` (UTF-8 بدون BOM).

```csharp
public Encoding Encoding { get; set; }
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
