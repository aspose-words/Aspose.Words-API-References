---
title: "Aspose::Words::Comparing::CompareOptions classe"
linktitle: "CompareOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::CompareOptions classe. Permet de choisir des options supplémentaires pour l'opération de comparaison de documents. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


Permet de choisir des options supplémentaires pour l'opération de comparaison de documents. Pour en savoir plus, consultez l'article de documentation [Compare Documents](https://docs.aspose.com/words/cpp/compare-documents/).

```cpp
class CompareOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | Spécifie des options de comparaison avancées qui peuvent aider à produire une sortie de comparaison plus précise. |
| [get_CompareMoves](./get_comparemoves/)() const | Spécifie s'il faut comparer les différences entre les deux documents. |
| [get_Granularity](./get_granularity/)() const | Spécifie si les modifications sont suivies par caractère ou par mot. |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | Vrai indique que la comparaison des documents n'est pas sensible à la casse. |
| [get_IgnoreComments](./get_ignorecomments/)() const | Spécifie s'il faut comparer les différences dans les commentaires. |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | Spécifie s'il faut ignorer la différence dans l'ID unique de DrawingML. |
| [get_IgnoreFields](./get_ignorefields/)() const | Spécifie s'il faut comparer les différences dans les champs. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Spécifie s'il faut comparer les différences dans les notes de bas de page et les notes de fin. |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | Vrai indique que le formatage est ignoré. |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | Vrai indique que le contenu des en-têtes et pieds de page est ignoré. |
| [get_IgnoreTables](./get_ignoretables/)() const | Spécifie s'il faut comparer les différences de données contenues dans les tableaux. |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | Spécifie s'il faut comparer les différences des données contenues dans les zones de texte. |
| [get_Target](./get_target/)() const | Spécifie quel document doit être utilisé comme cible lors de la comparaison. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/). |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/). |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/). |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/). |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | Mutateur pour [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/). |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | Définisseur de [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/). |
| [set_IgnoreTables](./set_ignoretables/)(bool) | Définisseur de [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/). |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | Définisseur de [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/). |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | Définisseur de [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment filtrer des types spécifiques d'éléments de document lors d'une comparaison.
```cpp
// Créez le document original et remplissez-le avec différents types d'éléments.
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// Texte du paragraphe référencé avec une note de bas de page :
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// Tableau :
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// Zone de texte :
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// Champ DATE :
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// Commentaire :
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// En-tête :
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// Créez un clone de notre document et effectuez une modification rapide sur chaque élément du document cloné.
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

// Comparer des documents crée une révision pour chaque modification du document édité.
// Un objet CompareOptions possède une série de drapeaux pouvant supprimer les révisions
// sur chaque type d'élément respectif, en ignorant effectivement leurs modifications.
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

## Voir aussi

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
