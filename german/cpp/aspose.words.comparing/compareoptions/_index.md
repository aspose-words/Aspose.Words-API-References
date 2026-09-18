---
title: "Aspose::Words::Comparing::CompareOptions class"
linktitle: "CompareOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comparing::CompareOptions class. Ermöglicht die Auswahl zusätzlicher Optionen für den Dokumentvergleichsvorgang. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


Ermöglicht die Auswahl zusätzlicher Optionen für den Dokumentvergleichsvorgang. Weitere Informationen finden Sie im Dokumentationsartikel [Compare Documents](https://docs.aspose.com/words/cpp/compare-documents/).

```cpp
class CompareOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | Gibt erweiterte Vergleichsoptionen an, die dabei helfen können, ein präziseres Vergleichsergebnis zu erzeugen. |
| [get_CompareMoves](./get_comparemoves/)() const | Gibt an, ob Unterschiede zwischen den beiden Dokumenten verglichen werden sollen. |
| [get_Granularity](./get_granularity/)() const | Gibt an, ob Änderungen Zeichenweise oder wortweise nachverfolgt werden. |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | True bedeutet, dass der Dokumentvergleich nicht zwischen Groß- und Kleinschreibung unterscheidet. |
| [get_IgnoreComments](./get_ignorecomments/)() const | Gibt an, ob Unterschiede in Kommentaren verglichen werden sollen. |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | Gibt an, ob Unterschiede in der eindeutigen DrawingML‑Id ignoriert werden sollen. |
| [get_IgnoreFields](./get_ignorefields/)() const | Gibt an, ob Unterschiede in Feldern verglichen werden sollen. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Gibt an, ob Unterschiede in Fußnoten und Endnoten verglichen werden sollen. |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | True bedeutet, dass die Formatierung ignoriert wird. |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | True gibt an, dass der Inhalt von Kopf- und Fußzeilen ignoriert wird. |
| [get_IgnoreTables](./get_ignoretables/)() const | Gibt an, ob die Unterschiede in den in Tabellen enthaltenen Daten verglichen werden sollen. |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | Gibt an, ob Unterschiede in den in Textfeldern enthaltenen Daten verglichen werden sollen. |
| [get_Target](./get_target/)() const | Gibt an, welches Dokument während des Vergleichs als Ziel verwendet werden soll. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/). |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | Setter für [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/). |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/). |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/). |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/). |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/). |
| [set_IgnoreTables](./set_ignoretables/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/). |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | Setter für [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/). |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | Setter für [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man bestimmte Arten von Dokumentelementen beim Vergleich filtert.
```cpp
// Erstellen Sie das Originaldokument und füllen Sie es mit verschiedenen Arten von Elementen.
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// Absatztext, der mit einer Endnote referenziert wird:
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// Tabelle:
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// Textfeld:
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// DATUM-Feld:
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// Kommentar:
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// Kopfzeile:
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// Erstellen Sie eine Kopie unseres Dokuments und führen Sie eine schnelle Bearbeitung jedes Elements des geklonten Dokuments durch.
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

// Der Vergleich von Dokumenten erstellt für jede Bearbeitung im bearbeiteten Dokument eine Revision.
// Ein CompareOptions-Objekt verfügt über eine Reihe von Flags, die Revisionen unterdrücken können
// für jeden jeweiligen Elementtyp, wodurch deren Änderungen effektiv ignoriert werden.
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

## Siehe auch

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
