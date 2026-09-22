---
title: "تعداد Aspose::Words::Saving::ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Saving::ExportHeadersFootersMode. يحدد كيفية تصدير الترويسات والتذييلات إلى HTML أو MHTML أو EPUB في C++."
type: docs
weight: 55000
url: /ar/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


يحدد كيفية تصدير رؤوس وتذييلات الصفحات إلى HTML أو MHTML أو EPUB.

```cpp
enum class ExportHeadersFootersMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لا يتم تصدير الترويسات والتذييلات. |
| لكل قسم | 1 | يتم تصدير رؤوس وتذييلات الصفحة الأساسية في بداية ونهاية كل قسم. |
| FirstSectionHeaderLastSectionFooter | 2 | يتم تصدير رأس الصفحة الأساسي للقسم الأول في بداية المستند وتذييل الصفحة الأساسي في النهاية. |
| FirstPageHeaderFooterPerSection | 3 | يتم تصدير رأس وتذييل الصفحة الأولى في بداية ونهاية كل قسم. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
