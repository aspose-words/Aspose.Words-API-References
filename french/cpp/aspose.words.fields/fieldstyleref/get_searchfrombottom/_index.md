---
title: "Aspose::Words::Fields::FieldStyleRef::get_SearchFromBottom méthode"
linktitle: "get_SearchFromBottom"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldStyleRef::get_SearchFromBottom method. Obtient ou définit si la recherche doit se faire à partir du bas de la page actuelle, plutôt qu'à partir du haut en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fields/fieldstyleref/get_searchfrombottom/
---
## FieldStyleRef::get_SearchFromBottom method


Obtient ou définit si la recherche doit commencer depuis le bas de la page actuelle, plutôt que depuis le haut.

```cpp
bool Aspose::Words::Fields::FieldStyleRef::get_SearchFromBottom()
```


## Exemples



Montre comment utiliser les champs STYLEREF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez une liste basée sur un modèle de liste Microsoft Word.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Cette liste générée affichera "1.a )".
// L'espace avant la parenthèse est un caractère non délimiteur, que nous pouvons supprimer.
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"\x0000" u".");
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"\x0001" u" )");

// Ajoutez du texte et appliquez des styles de paragraphe que les champs STYLEREF référenceront.
builder->get_ListFormat()->set_List(list);
builder->get_ListFormat()->ListIndent();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(u"Item 2");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 3");
builder->get_ListFormat()->RemoveNumbers();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Placez un champ STYLEREF dans l'en-tête et affichez le premier texte au style "List Paragraph" dans le document.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");

// Placez un champ STYLEREF dans le pied de page, et faites-le afficher le dernier texte.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");
field->set_SearchFromBottom(true);

builder->MoveToDocumentEnd();

// Nous pouvons également utiliser les champs STYLEREF pour référencer les numéros de listes.
builder->Write(u"\nParagraph number: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumber(true);

builder->Write(u"\nParagraph number, relative context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInRelativeContext(true);

builder->Write(u"\nParagraph number, full context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);

builder->Write(u"\nParagraph number, full context, non-delimiter chars suppressed: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);
field->set_SuppressNonDelimiters(true);

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.STYLEREF.docx");
```

## Voir aussi

* Class [FieldStyleRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
