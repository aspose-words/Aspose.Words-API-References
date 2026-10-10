---
title: "Aspose::Words::Document::get_RemovePersonalInformation metod"
linktitle: "get_RemovePersonalInformation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_RemovePersonalInformation metod. Hämtar eller anger en flagga som indikerar att Microsoft Word kommer att ta bort all användarinformation från kommentarer, revisioner och dokumentegenskaper när dokumentet sparas i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Hämtar eller anger en flagga som indikerar att Microsoft Word kommer att ta bort all användarinformation från kommentarer, revisioner och dokumentegenskaper när dokumentet sparas.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Exempel



Visar hur man aktiverar borttagning av personlig information under en manuell sparning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga lite innehåll med personlig information.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// Denna flagga motsvarar Fil -> Alternativ -> Säkerhetscenter -> Inställningar för Säkerhetscenter... ->
// Integritetsalternativ -> "Ta bort personlig information från filens egenskaper vid sparning" i Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// Detta alternativ kommer inte att träda i kraft under en sparoperation som görs med Aspose.Words.
// Personuppgifter kommer att tas bort från vårt dokument när flaggan är satt när vi sparar det manuellt med Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
