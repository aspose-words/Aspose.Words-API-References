---
title: Aspose::Words::Lists::List::get_IsRestartAtEachSection method
linktitle: get_IsRestartAtEachSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::List::get_IsRestartAtEachSection method. Specifies whether list should be restarted at each section. Default value is false in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Specifies whether list should be restarted at each section. Default value is **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Remarks


This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) is higher then [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Examples



Shows how to configure a list to restart numbering at each section. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// The "IsRestartAtEachSection" property will only be applicable when
// the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
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

## See Also

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
