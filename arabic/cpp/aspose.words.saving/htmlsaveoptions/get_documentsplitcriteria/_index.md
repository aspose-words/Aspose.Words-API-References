---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria"
linktitle: "get_DocumentSplitCriteria"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria. تحدد كيفية تقسيم المستند عند الحفظ إلى صيغة Html أو Epub أو Azw3. القيمة الافتراضية هي None لـ HTML و HeadingParagraph لـ EPUB و AZW3 في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


تحدد كيفية تقسيم المستند عند الحفظ إلى صيغة [Html](../../../aspose.words/saveformat/)، [Epub](../../../aspose.words/saveformat/) أو [Azw3](../../../aspose.words/saveformat/). القيمة الافتراضية هي [None](../../documentsplitcriteria/) لـ HTML و [HeadingParagraph](../../documentsplitcriteria/) لـ EPUB و AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## ملاحظات


عادةً ما ترغب في حفظ المستند إلى HTML كملف واحد. ولكن في بعض الحالات يفضل تقسيم الناتج إلى عدة صفحات HTML أصغر. عند حفظ بتنسيق HTML، سيتم إخراج هذه الصفحات إلى ملفات أو تدفقات منفصلة. عند حفظ بتنسيق EPUB سيتم دمجها في الحزم المقابلة.

لا يمكن تقسيم المستند عند الحفظ بتنسيق MHTML.

## أمثلة



يوضح كيفية استخدام ترميز محدد عند حفظ مستند إلى .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// استخدم كائن SaveOptions لتحديد الترميز للمستند الذي سنقوم بحفظه.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// بشكل افتراضي، سيحتوي مستند .epub الناتج على جميع محتوياته في جزء HTML واحد.
// معيار التقسيم يتيح لنا تقسيم المستند إلى عدة أجزاء HTML.
// سنحدد المعايير لتقسيم المستند إلى فقرات عناوين.
// هذا مفيد للقراء الذين لا يمكنهم قراءة ملفات HTML التي تتجاوز حجمًا معينًا.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// حدد أننا نريد تصدير خصائص المستند.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## انظر أيضًا

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
