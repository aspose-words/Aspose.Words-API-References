---
title: "Aspose::Words::Document::StartTrackRevisions metod"
linktitle: "StartTrackRevisions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::StartTrackRevisions metod. Påbörjar automatiskt märkning av alla framtida ändringar du gör i dokumentet programatiskt som revisionsändringar i C++."
type: docs
weight: 92000
url: /sv/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


Startar automatiskt märkning av alla ytterligare ändringar du gör i dokumentet programatiskt som revisionsändringar.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
## Anmärkningar


Om du anropar den här metoden och sedan gör några ändringar i dokumentet programatiskt, sparar dokumentet och senare öppnar dokumentet i MS Word kommer du att se dessa ändringar som revisioner.

För närvarande stödjer Aspose.Words endast spårning av nodinfogningar och -borttagningar. Formateringsändringar registreras inte som revisioner.

Automatisk spårning av ändringar stöds både när detta dokument modifieras genom nodmanipulationer samt när [DocumentBuilder](../../documentbuilder/) används.

Denna metod ändrar inte alternativet [TrackRevisions](../get_trackrevisions/) och använder inte dess värde för revisionsspårning.

## Exempel



Visar hur man spårar revisioner medan man redigerar ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Att redigera ett dokument räknas vanligtvis inte som en revision förrän vi börjar spåra dem.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Stoppa spårning av revisioner för att inte räkna framtida redigeringar som revisioner.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Att skapa revisioner ger dem ett datum och en tid för operationen.
// Vi kan inaktivera detta genom att skicka DateTime.MinValue när vi påbörjar spårning av revisioner.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Vi kan acceptera/avvisa dessa revisioner programmässigt
// genom att anropa metoder som Document.AcceptAllRevisions eller varje revisions Accept‑metod.
// I Microsoft Word kan vi bearbeta dem manuellt via \"Review\" -> \"Changes\".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


Startar automatiskt märkning av alla ytterligare ändringar du gör i dokumentet programatiskt som revisionsändringar.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| författare | const System::String\& | Initialer för författaren att använda för revisioner. |
| dateTime | System::DateTime | Datumet och tiden att använda för revisioner. |
## Anmärkningar


Om du anropar den här metoden och sedan gör några ändringar i dokumentet programatiskt, sparar dokumentet och senare öppnar dokumentet i MS Word kommer du att se dessa ändringar som revisioner.

För närvarande stödjer Aspose.Words endast spårning av nodinfogningar och -borttagningar. Formateringsändringar registreras inte som revisioner.

Automatisk spårning av ändringar stöds både när detta dokument modifieras genom nodmanipulationer samt när [DocumentBuilder](../../documentbuilder/) används.

Denna metod ändrar inte alternativet [TrackRevisions](../get_trackrevisions/) och använder inte dess värde för revisionsspårning.

## Exempel



Visar hur man spårar revisioner medan man redigerar ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Att redigera ett dokument räknas vanligtvis inte som en revision förrän vi börjar spåra dem.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Stoppa spårning av revisioner för att inte räkna framtida redigeringar som revisioner.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Att skapa revisioner ger dem ett datum och en tid för operationen.
// Vi kan inaktivera detta genom att skicka DateTime.MinValue när vi påbörjar spårning av revisioner.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Vi kan acceptera/avvisa dessa revisioner programmässigt
// genom att anropa metoder som Document.AcceptAllRevisions eller varje revisions Accept‑metod.
// I Microsoft Word kan vi bearbeta dem manuellt via \"Review\" -> \"Changes\".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
