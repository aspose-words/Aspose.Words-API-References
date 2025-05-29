---
title: SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية SaveFormat في SaveOptions لاختيار تنسيق حفظ مستندك بسهولة لتحقيق أقصى قدر من المرونة والتحكم.
type: docs
weight: 130
url: /ar/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
