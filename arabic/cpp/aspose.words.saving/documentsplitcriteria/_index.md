---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. يحدد كيفية تقسيم المستند إلى أجزاء عند الحفظ بتنسيق Html أو Epub أو Azw3 في C++."
type: docs
weight: 52000
url: /ar/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


يحدد كيفية تقسيم المستند إلى أجزاء عند الحفظ إلى تنسيق [Html](../../aspose.words/saveformat/)، [Epub](../../aspose.words/saveformat/) أو [Azw3](../../aspose.words/saveformat/).

```cpp
enum class DocumentSplitCriteria
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | المستند غير مقسَّم. |
| PageBreak | 1 | يتم تقسيم المستند إلى أجزاء عند فواصل الصفحات الصريحة. يمكن تحديد فاصل الصفحة بواسطة حرف [PageBreak](../../aspose.words/controlchar/pagebreak/)، أو فاصل قسم يحدد بدء قسم جديد في صفحة جديدة، أو فقرة لديها خاصية [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) مضبوطة على **true**. |
| ColumnBreak | 2 | يتم تقسيم المستند إلى أجزاء عند فواصل الأعمدة. يمكن تحديد فاصل العمود بواسطة حرف [ColumnBreak](../../aspose.words/controlchar/columnbreak/)، أو فاصل قسم يحدد بدء قسم جديد في عمود جديد. |
| SectionBreak | 4 | يتم تقسيم المستند إلى أجزاء عند فاصل قسم من أي نوع. |
| HeadingParagraph | 8 | يتم تقسيم المستند إلى أجزاء عند فقرة مُنسَّقة باستخدام نمط عنوان **Heading 1**، **Heading 2** إلخ. استخدم مع [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) لتحديد مستويات العناوين (من 1 إلى المستوى المحدد) التي يتم عندها التقسيم. |

## ملاحظات


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

يمكن أن تتداخل المعايير المختلفة جزئياً. على سبيل المثال، نمط **Heading 1** يُعطى غالباً خاصية [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) لذا فهو يندرج تحت معيارين: [PageBreak](./) و[HeadingParagraph](./). بعض فواصل الأقسام يمكن أن تُسبب فواصل صفحات وما إلى ذلك. في الحالات العادية، يكون تحديد علم واحد فقط هو الخيار الأكثر عملية.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
