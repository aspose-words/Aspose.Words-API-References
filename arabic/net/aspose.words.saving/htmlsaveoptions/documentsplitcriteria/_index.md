---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions DocumentSplitCriteria لتحسين حفظ المستندات بتنسيقات HTML وEPUB وAZW3. حسّن تحكمك في التنسيق اليوم!
type: docs
weight: 80
url: /ar/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

يحدد كيفية تقسيم المستند عند الحفظ فيHtml ، Epub أوAzw3 التنسيق الافتراضي هوNone لـ HTML و HeadingParagraph لـ EPUB وAZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## ملاحظات

عادةً ما تريد حفظ مستند بتنسيق HTML كملف واحد. ولكن في بعض الحالات يكون من الأفضل تقسيم الإخراج إلى عدة صفحات HTML أصغر. عند الحفظ بتنسيق HTML، سيتم إخراج هذه الصفحات إلى ملفات أو تدفقات فردية. عند الحفظ بتنسيق EPUB، سيتم دمجها في الحزم المقابلة.

لا يمكن تقسيم المستند عند الحفظ بتنسيق MHTML.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
