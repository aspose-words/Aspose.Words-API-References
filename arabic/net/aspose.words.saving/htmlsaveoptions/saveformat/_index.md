---
title: HtmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions SaveFormat ملكية. يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكونHtml Mhtml EpubAzw3 أوMobi  في C#.
type: docs
weight: 440
url: /ar/net/aspose.words.saving/htmlsaveoptions/saveformat/
---
## HtmlSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكونHtml ,Mhtml ,EpubAzw3 أوMobi .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## أمثلة

يوضح كيفية استخدام ترميز معين عند حفظ مستند إلى .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// استخدم كائن SaveOptions لتحديد ترميز المستند الذي سنقوم بحفظه.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// بشكل افتراضي، سيحتوي مستند الإخراج .epub على جميع محتوياته في جزء HTML واحد.
// يسمح لنا معيار التقسيم بتقسيم المستند إلى عدة أجزاء بتنسيق HTML.
// سنضع المعايير لتقسيم الوثيقة إلى فقرات رأسية.
// هذا مفيد للقراء الذين لا يستطيعون قراءة ملفات HTML ذات حجم أكبر من حجم معين.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// حدد أننا نريد تصدير خصائص المستند.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
