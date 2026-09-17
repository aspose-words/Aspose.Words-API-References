---
title: "Aspose::Words::Tables::CellFormat::get_Width méthode"
linktitle: "get_Width"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::CellFormat::get_Width méthode. Obtient la largeur de la cellule en points en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.tables/cellformat/get_width/
---
## CellFormat::get_Width method


Obtient la largeur de la cellule en points.

```cpp
double Aspose::Words::Tables::CellFormat::get_Width()
```

## Remarques


La largeur est calculée par Aspose.Words lors du chargement et de l'enregistrement du document. Actuellement, toutes les combinaisons de propriétés de tableau, de cellule et de document ne sont pas prises en charge. La valeur retournée peut ne pas être précise pour certains documents. Elle peut ne pas correspondre exactement à la largeur de la cellule telle que calculée par MS Word lorsque le document est ouvert dans MS Word.

La définition de cette propriété n'est pas recommandée. Il n'y a aucune garantie que la cellule aura réellement la largeur définie. La largeur peut être ajustée pour accueillir le contenu de la cellule dans une disposition de tableau à ajustement automatique. Les cellules d'autres lignes peuvent avoir des réglages de largeur conflictuels. Le tableau peut être redimensionné pour s'adapter au conteneur ou pour respecter les paramètres de largeur du tableau. Envisagez d'utiliser [PreferredWidth](../get_preferredwidth/) pour définir la largeur de la cellule. La définition de cette propriété définit implicitement [PreferredWidth](../get_preferredwidth/) depuis la version 15.8.

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


Montre comment formater les cellules avec un constructeur de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Insérez une deuxième cellule, puis configurez les options de remplissage du texte de la cellule.
// Le constructeur appliquera ces paramètres à la cellule actuelle, et toute nouvelle cellule créée par la suite.
builder->InsertCell();

System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = builder->get_CellFormat();
cellFormat->set_Width(250);
cellFormat->set_LeftPadding(30);
cellFormat->set_RightPadding(30);
cellFormat->set_TopPadding(30);
cellFormat->set_BottomPadding(30);

builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->EndTable();

// La première cellule n’a pas été affectée par la reconfiguration du remplissage, et conserve toujours les valeurs par défaut.
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_BottomPadding());

ASPOSE_ASSERT_EQ(250.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_BottomPadding());

// La première cellule continuera de s’agrandir dans le document de sortie pour correspondre à la taille de sa cellule voisine.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetCellFormatting.docx");
```

## Voir aussi

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
