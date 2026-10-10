---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection metodo"
linktitle: "get_IsRestartAtEachSection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection metodo. Specifica se l'elenco deve essere riavviato in ogni sezione. Il valore predefinito è false in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Specifica se l'elenco deve essere ricominciato in ogni sezione. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Note


Questa opzione è supportata solo nei formati di documento RTF, DOC e DOCX.

Questa opzione verrà scritta nel DOCX solo se [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) è più alta di [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Esempi



Mostra come configurare un elenco per riavviare la numerazione in ogni sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// La proprietà "IsRestartAtEachSection" sarà applicabile solo quando
// il livello di conformità OOXML del documento è impostato su uno standard più recente di "OoxmlComplianceCore.Ecma376".
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

## Vedi anche

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
