---
title: SaveOptions.SaveFormat
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


