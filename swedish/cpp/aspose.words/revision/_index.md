---
title: "Aspose::Words::Revision-klass"
linktitle: "Revision"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Revision-klass. Representerar en revision (spårad ändring) i ett dokumentnod eller stil. Använd RevisionType för att kontrollera typen av denna revision. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 52000
url: /sv/cpp/aspose.words/revision/
---
## Revision class


Representerar en revision (spårad ändring) i ett dokumentnod eller stil. Använd [RevisionType](./get_revisiontype/) för att kontrollera typen av denna revision. För att lära dig mer, besök dokumentationsartikeln [Spåra ändringar i ett dokument](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class Revision : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)() | Accepterar denna revision. |
| [get_Author](./get_author/)() | Hämtar eller anger författaren till denna revision. Får inte vara en tom sträng eller **null**. |
| [get_DateTime](./get_datetime/)() | Hämtar eller anger datum/tid för denna revision. |
| [get_Group](./get_group/)() | Hämtar revisionsgruppen. Returnerar **null** om revisionen inte tillhör någon grupp. |
| [get_ParentNode](./get_parentnode/)() | Hämtar den omedelbara föräldranoden (ägare) för denna revision. Denna egenskap fungerar för alla revisionstyper förutom [StyleDefinitionChange](../revisiontype/). |
| [get_ParentStyle](./get_parentstyle/)() | Hämtar den omedelbara förälderstilen (ägare) för denna revision. Denna egenskap fungerar endast för [StyleDefinitionChange](../revisiontype/) revisionstyp. |
| [get_RevisionType](./get_revisiontype/)() const | Hämtar typen av denna revision. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Reject](./reject/)() | Avvisa denna revision. |
| [set_Author](./set_author/)(const System::String\&) | Sättare för [Aspose::Words::Revision::get_Author](./get_author/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Sättare för [Aspose::Words::Revision::get_DateTime](./get_datetime/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man arbetar med revisioner i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normal redigering av dokumentet räknas inte som en revision.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// För att registrera våra ändringar som revisioner måste vi deklarera en författare och sedan börja spåra dem.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// Denna flagga motsvarar alternativet "Review" -> "Tracking" -> "Track Changes" i Microsoft Word.
// "StartTrackRevisions"-metoden påverkar inte dess värde,
// och dokumentet spårar revisioner programatiskt trots att det har värdet "false".
// Om vi öppnar detta dokument med Microsoft Word kommer det inte att spåra revisioner.
ASSERT_FALSE(doc->get_TrackRevisions());

// Vi har lagt till text med dokumentbyggaren, så den första revisionen är en insättningsrevision.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Ta bort ett run för att skapa en raderingsrevision.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Att lägga till en ny revision placerar den i början av revisionssamlingen.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Infogningsrevisioner visas i dokumentkroppen redan innan vi accepterar/avvisar revisionen.
// Att avvisa revisionen tar bort dess noder från kroppen. Omvänt, noder som utgör raderingsrevisioner
// ligger också kvar i dokumentet tills vi accepterar revisionen.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Att acceptera raderingsrevisionen tar bort dess föräldranod från stycketexten
// och tar sedan bort revisionen från samlingen.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Flytta nu noden för att skapa en flyttningsrevision.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// Den rörliga revisionen är nu på index 1. Avvisa revisionen för att kassera dess innehåll.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
