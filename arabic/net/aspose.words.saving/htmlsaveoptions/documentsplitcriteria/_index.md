---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد كيفية تقسيم المستند عند الحفظ فيهHtmlEpub أوAzw3 شكل. الافتراضي هوNone لـ HTML و HeadingParagraph لـ EPUB وAZW3.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

يحدد كيفية تقسيم المستند عند الحفظ فيهHtmlEpub أوAzw3 شكل. الافتراضي هوNone لـ HTML و HeadingParagraph لـ EPUB وAZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### ملاحظات

عادةً ما تريد حفظ مستند بتنسيق HTML كملف واحد. ولكن في بعض الحالات يفضل تقسيم المخرجات إلى عدة صفحات HTML أصغر. عند الحفظ بتنسيق HTML، سيتم إخراج هذه الصفحات إلى ملفات أو تدفقات فردية. عند الحفظ بتنسيق EPUB، سيتم دمجها في الحزم المقابلة.

لا يمكن تقسيم المستند عند حفظه بتنسيق MHTML.

### أمثلة

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


