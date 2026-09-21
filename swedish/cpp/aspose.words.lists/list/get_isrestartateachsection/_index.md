---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection method"
linktitle: "get_IsRestartAtEachSection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection metod. Anger om listan ska startas om i varje avsnitt. Standardvärdet är falskt i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Anger om listan ska startas om i varje avsnitt. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Anmärkningar


Detta alternativ stöds endast i dokumentformaten RTF, DOC och DOCX.

Detta alternativ kommer att skrivas till DOCX endast om [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) är högre än [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Exempel



Visar hur man konfigurerar en lista för att starta om numreringen i varje avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// Egenskapen "IsRestartAtEachSection" kommer endast att vara tillämplig när
// dokumentets OOXML-efterlevnadsnivå är en standard som är nyare än "OoxmlComplianceCore.Ecma376".
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

## Se även

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
