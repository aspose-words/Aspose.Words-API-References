---
title: "Classe Aspose::Words::Comparing::CompareOptions"
linktitle: "CompareOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Comparing::CompareOptions. Consente di scegliere opzioni aggiuntive per l'operazione di confronto dei documenti. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


Consente di scegliere opzioni aggiuntive per l'operazione di confronto dei documenti. Per saperne di più, visita l'articolo di documentazione [Confronta documenti](https://docs.aspose.com/words/cpp/compare-documents/).

```cpp
class CompareOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | Specifica opzioni di confronto avanzate che potrebbero aiutare a produrre un output di confronto più preciso. |
| [get_CompareMoves](./get_comparemoves/)() const | Specifica se confrontare le differenze tra i due documenti. |
| [get_Granularity](./get_granularity/)() const | Specifica se le modifiche sono tracciate per carattere o per parola. |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | True indica che il confronto dei documenti non distingue maiuscole/minuscole. |
| [get_IgnoreComments](./get_ignorecomments/)() const | Specifica se confrontare le differenze nei commenti. |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | Specifica se ignorare le differenze nell'Id univoco di DrawingML. |
| [get_IgnoreFields](./get_ignorefields/)() const | Specifica se confrontare le differenze nei campi. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Specifica se confrontare le differenze in note a piè di pagina e note finali. |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | True indica che la formattazione è ignorata. |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | True indica che il contenuto di intestazioni e piè di pagina è ignorato. |
| [get_IgnoreTables](./get_ignoretables/)() const | Specifica se confrontare le differenze nei dati contenuti nelle tabelle. |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | Specifica se confrontare le differenze nei dati contenuti nelle caselle di testo. |
| [get_Target](./get_target/)() const | Specifica quale documento deve essere usato come destinazione durante il confronto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | Setter per [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/). |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | Setter per [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/). |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | Setter per [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/). |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | Setter per [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/). |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Setter per [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Setter per [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Setter per [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | Setter per [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/). |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | Impostatore per [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/). |
| [set_IgnoreTables](./set_ignoretables/)(bool) | Impostatore per [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/). |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | Impostatore per [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/). |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | Impostatore per [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come filtrare tipi specifici di elementi del documento durante un confronto.
```cpp
// Crea il documento originale e popolalo con vari tipi di elementi.
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// Testo del paragrafo riferito con una nota a piè di pagina:
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// Tabella:
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// Casella di testo:
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// Campo DATE:
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// Commento:
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// Intestazione:
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// Crea una copia del nostro documento ed esegui una modifica rapida su ciascuno degli elementi del documento clonato.
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

// Il confronto dei documenti crea una revisione per ogni modifica nel documento modificato.
// Un oggetto CompareOptions ha una serie di flag che possono sopprimere le revisioni
// su ogni tipo rispettivo di elemento, ignorando efficacemente le loro modifiche.
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

## Vedi anche

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
