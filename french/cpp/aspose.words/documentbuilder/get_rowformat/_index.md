---
title: "Aspose::Words::DocumentBuilder::get_RowFormat méthode"
linktitle: "get_RowFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_RowFormat méthode. Retourne un objet qui représente les propriétés de formatage de la ligne de tableau actuelle en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words/documentbuilder/get_rowformat/
---
## DocumentBuilder::get_RowFormat method


Renvoie un objet qui représente les propriétés de mise en forme de la ligne de tableau actuelle.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowFormat> Aspose::Words::DocumentBuilder::get_RowFormat()
```


## Exemples



Montre comment construire un tableau avec des bordures personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Définition des options de formatage de tableau pour un DocumentBuilder
// les appliquera à chaque ligne et cellule que nous ajoutons avec celui‑ci.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Modifier le formatage l'appliquera à la cellule actuelle,
// et à toutes les nouvelles cellules que nous créons avec le constructeur par la suite.
// Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Augmentez la hauteur de la ligne pour adapter le texte vertical.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Montre comment créer un tableau formaté 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Lors de la création du tableau, le constructeur de document appliquera les valeurs actuelles de ses propriétés RowFormat/CellFormat.
// à la ligne/colonne actuelle où se trouve le curseur ainsi qu'aux nouvelles lignes/colonnes créées.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Les lignes et cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications du formatage du constructeur.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


Montre comment formater des lignes avec un constructeur de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Commencez une deuxième ligne, puis configurez sa hauteur. Le constructeur appliquera ces paramètres à
// sa ligne actuelle, ainsi qu’à toutes les nouvelles lignes qu’il crée par la suite.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// La première ligne n’a pas été affectée par la reconfiguration du remplissage et conserve toujours les valeurs par défaut.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Voir aussi

* Class [RowFormat](../../../aspose.words.tables/rowformat/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
