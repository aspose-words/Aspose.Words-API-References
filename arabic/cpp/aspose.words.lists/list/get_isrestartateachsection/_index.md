---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection طريقة"
linktitle: "get_IsRestartAtEachSection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection طريقة. يحدد ما إذا كان يجب إعادة تشغيل القائمة في كل قسم. القيمة الافتراضية هي false في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


يحدد ما إذا كان يجب إعادة بدء القائمة في كل قسم. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## ملاحظات


هذا الخيار مدعوم فقط في صيغ المستندات RTF و DOC و DOCX.

سيتم كتابة هذا الخيار إلى DOCX فقط إذا كان [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) أعلى من [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## أمثلة



يوضح كيفية تكوين قائمة لإعادة بدء الترقيم في كل قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// خاصية "IsRestartAtEachSection" ستكون صالحة فقط عندما
// مستوى امتثال OOXML للمستند هو معيار أحدث من "OoxmlComplianceCore.Ecma376".
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```

## انظر أيضًا

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
