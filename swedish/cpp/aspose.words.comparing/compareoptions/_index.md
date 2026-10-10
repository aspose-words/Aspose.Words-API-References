---
title: "Aspose::Words::Comparing::CompareOptions class"
linktitle: "CompareOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comparing::CompareOptions-klass. Tillåter att välja ytterligare alternativ för dokumentjämförelseoperationen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


Tillåter att välja ytterligare alternativ för dokumentjämförelseoperationen. För att läsa mer, besök dokumentationsartikeln [Compare Documents](https://docs.aspose.com/words/cpp/compare-documents/).

```cpp
class CompareOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | Anger avancerade jämförelsealternativ som kan hjälpa till att producera mer exakt jämförelsesresultat. |
| [get_CompareMoves](./get_comparemoves/)() const | Anger om skillnader mellan de två dokumenten ska jämföras. |
| [get_Granularity](./get_granularity/)() const | Anger om ändringar spåras per tecken eller per ord. |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | Sant indikerar att dokumentjämförelsen är skiftlägesokänslig. |
| [get_IgnoreComments](./get_ignorecomments/)() const | Anger om skillnader i kommentarer ska jämföras. |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | Anger om skillnad i DrawingML unika Id ska ignoreras. |
| [get_IgnoreFields](./get_ignorefields/)() const | Anger om skillnader i fält ska jämföras. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Anger om skillnader i fotnoter och slutnoter ska jämföras. |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | Sant indikerar att formatering ignoreras. |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | True indikerar att innehållet i sidhuvuden och sidfötter ignoreras. |
| [get_IgnoreTables](./get_ignoretables/)() const | Anger om skillnader i data som finns i tabeller ska jämföras. |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | Anger om skillnader i data som finns i textrutor ska jämföras. |
| [get_Target](./get_target/)() const | Anger vilket dokument som ska användas som mål under jämförelsen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/). |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/). |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/). |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/). |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/). |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/). |
| [set_IgnoreTables](./set_ignoretables/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/). |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/). |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | Inställare för [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man filtrerar specifika typer av dokumentelement när man gör en jämförelse.
```cpp
// Skapa originaldokumentet och fyll det med olika typer av element.
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// Paragraftext refererad med en slutnot:
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// Tabell:
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// Textruta:
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// DATUM-fält:
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// Kommentar:
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// Sidhuvud:
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// Skapa en klon av vårt dokument och utför en snabb redigering på varje element i det klonade dokumentet.
auto docEdited = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(docOriginal)->Clone(true));
System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = docEdited->get_FirstSection()->get_Body()->get_FirstParagraph();

firstParagraph->get_Runs()->idx_get(0)->set_Text(u"hello world! this is the first paragraph, after editing.");
firstParagraph->get_ParagraphFormat()->set_Style(docEdited->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1));
(System::ExplicitCast<Aspose::Words::Notes::Footnote>(docEdited->GetChild(Aspose::Words::NodeType::Footnote, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(1)->set_Text(u"Edited endnote text.");
(System::ExplicitCast<Aspose::Words::Tables::Table>(docEdited->GetChild(Aspose::Words::NodeType::Table, 0, true)))->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited Cell 2 contents");
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(docEdited->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited textbox contents");
(System::ExplicitCast<Aspose::Words::Fields::FieldDate>(docEdited->get_Range()->get_Fields()->idx_get(0)))->set_UseLunarCalendar(true);
(System::ExplicitCast<Aspose::Words::Comment>(docEdited->GetChild(Aspose::Words::NodeType::Comment, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited comment.");
docEdited->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited header contents.");

// Jämförelse av dokument skapar en revision för varje redigering i det redigerade dokumentet.
// Ett CompareOptions-objekt har en serie flaggor som kan undertrycka revisioner
// för varje respektive typ av element, vilket effektivt ignorerar deras förändring.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_CompareMoves(false);
compareOptions->set_IgnoreFormatting(false);
compareOptions->set_IgnoreCaseChanges(false);
compareOptions->set_IgnoreComments(false);
compareOptions->set_IgnoreTables(false);
compareOptions->set_IgnoreFields(false);
compareOptions->set_IgnoreFootnotes(false);
compareOptions->set_IgnoreTextboxes(false);
compareOptions->set_IgnoreHeadersAndFooters(false);
compareOptions->set_Target(Aspose::Words::Comparing::ComparisonTargetType::New);

docOriginal->Compare(docEdited, u"John Doe", System::DateTime::get_Now(), compareOptions);
docOriginal->Save(get_ArtifactsDir() + u"Revision.CompareOptions.docx");
```

## Se även

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
