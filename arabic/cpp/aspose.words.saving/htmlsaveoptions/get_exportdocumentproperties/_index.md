---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties"
linktitle: "get_ExportDocumentProperties"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties. تحدد ما إذا كان سيتم تصدير خصائص المستند المدمجة والمخصصة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي false في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportdocumentproperties/
---
## HtmlSaveOptions::get_ExportDocumentProperties method


يحدد ما إذا كان سيتم تصدير خصائص المستند المدمجة والمخصصة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties() const
```


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

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
