---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode طريقة"
linktitle: "get_ExportHeadersFootersMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode طريقة. يحدد كيفية إخراج رؤوس وتذييلات الصفحات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي PerSection لـ HTML/MHTML و None لـ EPUB في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


يحدد كيفية إخراج رؤوس وتذييلات الصفحات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [PerSection](../../exportheadersfootersmode/) لـ HTML/MHTML و [None](../../exportheadersfootersmode/) لـ EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## ملاحظات


من الصعب إخراج الرؤوس والتذييلات إلى HTML بشكل ملائم لأن HTML غير مُرقم.

عند كون هذه الخاصية [PerSection](../../exportheadersfootersmode/)، تقوم Aspose.Words بتصدير فقط الرؤوس والتذييلات الأساسية في بداية ونهاية كل قسم.

عند كونها [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) يتم تصدير فقط أول رأس أساسي وآخر تذييل أساسي (بما في ذلك المرتبط بالسابقة).

يمكنك تعطيل تصدير الرؤوس والتذييلات تمامًا عن طريق ضبط هذه الخاصية إلى [None](../../exportheadersfootersmode/).

## أمثلة



يوضح كيفية حذف الرؤوس/التذييلات عند حفظ المستند كـ HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// يحتوي هذا المستند على رؤوس وتذييلات. يمكننا الوصول إليها عبر مجموعة "HeadersFooters".
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// الصيغ مثل .html لا تقسم المستند إلى صفحات، لذا لن تعمل الرؤوس/التذييلات بنفس الطريقة.
// كما يحدث عندما نفتح المستند كملف .docx باستخدام Microsoft Word.
// إذا قمنا بتحويل مستند يحتوي على رؤوس/تذييلات إلى html، فإن التحويل سيدمج الرؤوس/التذييلات في نص الجسم.
// يمكننا استخدام كائن SaveOptions لحذف الرؤوس/التذييلات أثناء التحويل إلى html.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// افتح المستند المحفوظ وتأكد من أنه لا يحتوي على نص الرأس.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## انظر أيضًا

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
