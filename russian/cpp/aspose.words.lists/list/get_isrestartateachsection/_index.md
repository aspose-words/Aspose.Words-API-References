---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection метод"
linktitle: "get_IsRestartAtEachSection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection метод. Указывает, следует ли перезапускать список в каждом разделе. Значение по умолчанию — false в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Указывает, следует ли перезапускать список в каждом разделе. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Примечания


Эта опция поддерживается только в форматах документов RTF, DOC и DOCX.

Эта опция будет записана в DOCX только если [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) выше, чем [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Примеры



Показывает, как настроить список для перезапуска нумерации в каждом разделе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// Свойство "IsRestartAtEachSection" будет применимо только когда
// уровень соответствия OOXML документа соответствует стандарту, новее чем "OoxmlComplianceCore.Ecma376".
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

## См. также

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
