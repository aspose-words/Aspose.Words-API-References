---
title: "Aspose::Words::DocumentBuilder::get_ParagraphFormat method"
linktitle: "get_ParagraphFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_ParagraphFormat method. Retourne un objet qui représente les propriétés de formatage de paragraphe actuelles en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words/documentbuilder/get_paragraphformat/
---
## DocumentBuilder::get_ParagraphFormat method


Renvoie un objet qui représente les propriétés de mise en forme du paragraphe actuel.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::DocumentBuilder::get_ParagraphFormat()
```


## Exemples



Montre comment créer une table formatée en utilisant [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// Définissez quelques options de formatage pour le texte et l'apparence de la table.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// Configurer les options de formatage dans un constructeur de document les appliquera
// à la cellule/ligne actuelle où se trouve le curseur,
// ainsi qu'à toutes nouvelles cellules et lignes créées avec ce constructeur.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// Reconfigurez les objets de formatage du constructeur pour les nouvelles lignes et cellules que nous allons créer.
// Le builder ne les appliquera pas à la première ligne déjà créée afin qu'elle se démarque comme ligne d'en-tête.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```

## Voir aussi

* Class [ParagraphFormat](../../paragraphformat/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
