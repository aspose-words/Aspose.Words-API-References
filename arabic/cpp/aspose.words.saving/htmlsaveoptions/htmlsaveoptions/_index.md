---
title: "منشئ Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions"
linktitle: "HtmlSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions. يهيئ مثيلاً جديداً لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق Html في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/htmlsaveoptions/
---
## HtmlSaveOptions::HtmlSaveOptions() constructor


يهيئ مثيلاً جديداً لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Html](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions()
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
## HtmlSaveOptions::HtmlSaveOptions(Aspose::Words::SaveFormat) constructor


يهيئ مثيلاً جديداً لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Html](../../../aspose.words/saveformat/)، [Mhtml](../../../aspose.words/saveformat/)، [Epub](../../../aspose.words/saveformat/)، [Azw3](../../../aspose.words/saveformat/) أو [Mobi](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | يمكن أن يكون [Html](../../../aspose.words/saveformat/)، [Mhtml](../../../aspose.words/saveformat/)، [Epub](../../../aspose.words/saveformat/)، [Azw3](../../../aspose.words/saveformat/) أو [Mobi](../../../aspose.words/saveformat/). |

## أمثلة



يوضح كيفية حفظ مستند إلى إصدار محدد من HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(htmlVersion);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html", options);

// ستحتوي مستندات HTML الخاصة بنا على اختلافات طفيفة لتكون متوافقة مع إصدارات HTML المختلفة.
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case Aspose::Words::Saving::HtmlVersion::Html5:
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<table style=\"padding:0pt; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;

    case Aspose::Words::Saving::HtmlVersion::Xhtml:
        ASSERT_TRUE(outDocContents.Contains(u"<a name=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;

}
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
