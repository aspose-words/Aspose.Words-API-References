---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding method"
linktitle: "get_Encoding"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding method. يحدد الترميز الذي يُستخدم عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي new UTF8Encoding(false) (UTF-8 بدون BOM) في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_encoding/
---
## HtmlSaveOptions::get_Encoding method


يحدد الترميز المستخدم عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **new UTF8Encoding(false)** (UTF-8 بدون BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlSaveOptions::get_Encoding() const
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
