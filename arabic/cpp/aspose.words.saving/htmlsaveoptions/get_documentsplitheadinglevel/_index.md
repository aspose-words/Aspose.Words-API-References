---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel."
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel. تحدد الحد الأقصى لمستوى العناوين التي يتم عندها تقسيم المستند. القيمة الافتراضية هي %2 في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


يحدد الحد الأقصى لمستوى العناوين التي يتم عندها تقسيم المستند. القيمة الافتراضية هي **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## ملاحظات


عند تضمين [DocumentSplitCriteria](../get_documentsplitcriteria/) لـ [HeadingParagraph](../../documentsplitcriteria/) وتعيين هذه الخاصية إلى قيمة من 1 إلى 9، سيتم تقسيم المستند عند الفقرات المنسقة باستخدام أنماط **Heading 1**، **Heading 2**، **Heading 3** وما إلى ذلك حتى مستوى العنوان المحدد.

بشكل افتراضي، فقط فقرات **Heading 1** و**Heading 2** تتسبب في تقسيم المستند. تعيين هذه الخاصية إلى صفر سيمنع تقسيم المستند عند فقرات العناوين تمامًا.

## أمثلة



يوضح كيفية تقسيم مستند HTML الناتج حسب العناوين إلى عدة أجزاء.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// كل فقرة نقوم بتنسيقها باستخدام نمط "Heading" يمكن أن تكون عنوانًا.
// كل عنوان قد يكون له أيضًا مستوى عنوان، يتم تحديده بعدد نمط العنوان الخاص به.
// العناوين أدناه هي من المستويات 1-3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// أنشئ كائن HtmlSaveOptions واضبط معيار التقسيم إلى "HeadingParagraph".
// ستقوم هذه المعايير بتقسيم المستند عند الفقرات ذات أنماط "Heading" إلى عدة مستندات أصغر،
// وتحفظ كل مستند في ملف HTML منفصل في نظام الملفات المحلي.
// سنقوم أيضًا بتعيين الحد الأقصى لمستوى العنوان، والذي يقسم المستند إلى 2.
// سيؤدي حفظ المستند إلى تقسيمه عند العناوين من المستويات 1 و2، لكن ليس عند 3 إلى 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// مستندنا يحتوي على أربعة عناوين من المستويات 1 - 2. أحد هذه العناوين لن يكون
// نقطة تقسيم لأنها في بداية المستند.
// ستقوم عملية الحفظ بتقسيم مستندنا إلى ثلاث نقاط، إلى أربعة مستندات أصغر.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
