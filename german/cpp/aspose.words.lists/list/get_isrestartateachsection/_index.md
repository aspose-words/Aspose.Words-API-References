---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection Methode"
linktitle: "get_IsRestartAtEachSection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection Methode. Gibt an, ob die Liste am Anfang jedes Abschnitts neu gestartet werden soll. Der Standardwert ist false in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Gibt an, ob die Liste am Anfang jedes Abschnitts neu gestartet werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Hinweise


Diese Option wird nur in den Dokumentformaten RTF, DOC und DOCX unterstützt.

Diese Option wird nur in DOCX geschrieben, wenn [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) höher ist als [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Beispiele



Zeigt, wie man eine Liste so konfiguriert, dass die Nummerierung in jedem Abschnitt neu beginnt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// Die "IsRestartAtEachSection"‑Eigenschaft ist nur anwendbar, wenn
// das OOXML‑Compliance‑Level des Dokuments einem Standard entspricht, der neuer ist als "OoxmlComplianceCore.Ecma376".
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

## Siehe auch

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
