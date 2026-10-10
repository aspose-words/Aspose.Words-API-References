---
title: "Énumération Aspose::Words::Markup::SdtType"
linktitle: "SdtType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Markup::SdtType. Spécifie le type d'un nœud de balise de document structuré (SDT) en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


Spécifie le type d'un nœud de balise de document structuré (SDT).

```cpp
enum class SdtType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucun type n'est attribué au SDT. |
| Bibliographie | 1 | Le SDT représente une entrée de bibliographie. |
| Citation | 2 | Le SDT représente une citation. |
| Équation | 3 | Le SDT représente une équation. |
| DropDownList | 4 | Le SDT représente une liste déroulante lorsqu'elle est affichée dans le document. |
| ComboBox | 5 | Le SDT représente une zone combinée lorsqu'elle est affichée dans le document. |
| Date | 6 | Le SDT représente un sélecteur de date lorsqu'il est affiché dans le document. |
| BuildingBlockGallery | 7 | Le SDT représente un type de galerie de blocs de construction. |
| DocPartObj | 8 | Le SDT représente un type de partie de document. |
| Group | 9 | Le SDT représente un regroupement restreint lorsqu'il est affiché dans le document. |
| Picture | 10 | Le SDT représente une image lorsqu'elle est affichée dans le document. |
| RichText | 11 | Le SDT représente une zone de texte enrichi lorsqu'elle est affichée dans le document. |
| PlainText | 12 | Le SDT représente une zone de texte simple lorsqu'elle est affichée dans le document. |
| Checkbox | 13 | Le SDT représente une case à cocher lorsqu'elle est affichée dans le document. |
| RepeatingSection | 14 | Le SDT représente un type de section répétitive lorsqu'il est affiché dans le document. |
| RepeatingSectionItem | 15 | Le SDT représente un élément de section répétitive. |
| EntityPicker | 16 | Le SDT représente un sélecteur d'entité qui permet à l'utilisateur de choisir une instance d'un type de contenu externe. |


## Exemples



Montre comment travailler avec les styles pour les éléments de contrôle de contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous deux façons d'appliquer un style du document à une balise de document structuré.
// 1 -  Appliquer un objet de style provenant de la collection de styles du document :
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Référencer un style dans le document par son nom :
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```


Montre comment remplir un tableau avec des données provenant d'une partie XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// Créez des en-têtes pour les données provenant du contenu XML.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// Créer un tableau avec une section répétitive à l'intérieur.
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// Ajouter un élément de section répétitive à l'intérieur de la section répétitive et le marquer comme une ligne.
// Ce tableau aura une ligne pour chaque élément que nous pouvons trouver dans le document XML.
// en utilisant le XPath "/books[1]/book", dont il y en a trois.
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Mapper les données XML avec les cellules de tableau créées pour le titre et l'auteur de chaque livre.
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


Montre comment créer une balise de document structuré de groupe au niveau de la ligne.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Créer une balise de document structuré de groupe au niveau de la ligne.
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// Créer une ligne enfant de la balise de document structuré.
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// Insérer le contenu des cellules.
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// Insérer du texte après le tableau.
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


Montre comment créer une balise de document structuré de type Citation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// Créer un champ Citation.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// Déplacer le champ vers la balise de document structuré.
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
