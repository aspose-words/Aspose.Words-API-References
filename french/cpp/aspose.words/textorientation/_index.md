---
title: "Aspose::Words::TextOrientation enum"
linktitle: "TextOrientation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextOrientation enum. Spécifie l'orientation du texte sur une page, dans une cellule de tableau ou dans un cadre de texte en C++."
type: docs
weight: 124000
url: /fr/cpp/aspose.words/textorientation/
---
## TextOrientation enum


Spécifie l'orientation du texte sur une page, dans une cellule de tableau ou un cadre de texte.

```cpp
enum class TextOrientation
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Horizontal | 0 | Le texte est disposé horizontalement (lr-tb). |
| Vers le bas | 1 | Le texte est pivoté de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl). |
| Vers le haut | 3 | Le texte est pivoté de 90 degrés vers la gauche pour apparaître de bas en haut (bt-lr). |
| HorizontalRotatedFarEast | 4 | Le texte est disposé horizontalement, mais les caractères d'Extrême-Orient sont pivotés de 90 degrés vers la gauche (lr-tb-v). |
| VerticalFarEast | 5 | Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est pivoté de 90 degrés vers la droite pour s'afficher de haut en bas (tb-rl-v). |
| VerticalRotatedFarEast | 7 | Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est pivoté de 90 degrés vers la droite pour s'afficher de haut en bas verticalement, puis de gauche à droite horizontalement (tb-lr-v). |


## Exemples



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

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
