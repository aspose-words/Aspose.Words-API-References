---
title: "Aspose::Words::Comparing::CompareOptions::get_CompareMoves méthode"
linktitle: "get_CompareMoves"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comparing::CompareOptions::get_CompareMoves méthode. Spécifie s'il faut comparer les différences entre les deux documents en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.comparing/compareoptions/get_comparemoves/
---
## CompareOptions::get_CompareMoves method


Spécifie s'il faut comparer les différences entre les deux documents.

```cpp
bool Aspose::Words::Comparing::CompareOptions::get_CompareMoves() const
```


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

* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
