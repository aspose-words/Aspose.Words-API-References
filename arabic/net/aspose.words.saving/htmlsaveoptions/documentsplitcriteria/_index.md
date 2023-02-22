---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد كيفية تقسيم المستند عند الحفظHtml أوEpub صيغة. الافتراضي هوNone لـ HTML و HeadingParagraph لـ EPUB.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

يحدد كيفية تقسيم المستند عند الحفظHtml أوEpub صيغة. الافتراضي هوNone لـ HTML و HeadingParagraph لـ EPUB.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### ملاحظات

عادةً ما ترغب في حفظ مستند بتنسيق HTML كملف واحد. لكن في بعض الحالات يفضل تقسيم الإخراج إلى عدة صفحات HTML أصغر. عند الحفظ بتنسيق HTML ، سيتم إخراج هذه الصفحات إلى الملفات الفردية أو التدفقات. عند الحفظ بتنسيق EPUB ، سيتم دمجها في الحزم المقابلة.

لا يمكن تقسيم المستند عند الحفظ بتنسيق MHTML.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


