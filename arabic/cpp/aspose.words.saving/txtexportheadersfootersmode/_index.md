---
title: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum"
linktitle: "TxtExportHeadersFootersMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum. يحدد الطريقة التي يتم بها تصدير رؤوس وتذييلات الصفحات إلى تنسيق النص العادي في C++."
type: docs
weight: 86000
url: /ar/cpp/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enum


يحدد طريقة تصدير رؤوس وتذييلات الصفحات إلى تنسيق النص العادي.

```cpp
enum class TxtExportHeadersFootersMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لا يتم تصدير أي رؤوس أو تذييلات. |
| PrimaryOnly | 1 | يتم تصدير الرؤوس والتذييلات الأساسية فقط في بداية ونهاية كل قسم. |
| AllAtEnd | 2 | يتم وضع جميع الرؤوس والتذييلات بعد جميع محتويات الأقسام في نهاية المستند. |


## أمثلة



يظهر كيفية تحديد طريقة تصدير الرؤوس والتذييلات إلى تنسيق النص العادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// إدراج رؤوس/تذييلات زوجية وأساسية في المستند.
// ستتجاوز الرؤوس/التذييلات الأساسية الرؤوس/التذييلات الزوجية.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// إدراج صفحات لعرض هذه الرؤوس والتذييلات.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// عيّن الخاصية "ExportHeadersFootersMode" إلى "TxtExportHeadersFootersMode.None"
// لعدم تصدير أي رؤوس/تذييلات.
// عيّن الخاصية "ExportHeadersFootersMode" إلى "TxtExportHeadersFootersMode.PrimaryOnly"
// لتصدير الرؤوس/التذييلات الأساسية فقط.
// عيّن الخاصية "ExportHeadersFootersMode" إلى "TxtExportHeadersFootersMode.AllAtEnd"
// لوضع جميع رؤوس وتذييلات جميع أجسام الأقسام في نهاية المستند.
saveOptions->set_ExportHeadersFootersMode(txtExportHeadersFootersMode);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt");

System::String newLine = System::Environment::get_NewLine();
switch (txtExportHeadersFootersMode)
{
    case Aspose::Words::Saving::TxtExportHeadersFootersMode::AllAtEnd:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Even header{0}{1}", newLine, newLine) + System::String::Format(u"Primary header{0}{1}", newLine, newLine) + System::String::Format(u"Even footer{0}{1}", newLine, newLine) + System::String::Format(u"Primary footer{0}{1}", newLine, newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::PrimaryOnly:
        ASSERT_EQ(System::String::Format(u"Primary header{0}", newLine) + System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Primary footer{0}", newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::None:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine), docText);
        break;

}
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
