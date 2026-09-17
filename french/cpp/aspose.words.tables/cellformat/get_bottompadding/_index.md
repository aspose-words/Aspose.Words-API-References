---
title: "Méthode Aspose::Words::Tables::CellFormat::get_BottomPadding"
linktitle: "get_BottomPadding"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::CellFormat::get_BottomPadding. Retourne ou définit la quantité d'espace (en points) à ajouter sous le contenu de la cellule en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.tables/cellformat/get_bottompadding/
---
## CellFormat::get_BottomPadding method


Renvoie ou définit la quantité d'espace (en points) à ajouter sous le contenu de la cellule.

```cpp
double Aspose::Words::Tables::CellFormat::get_BottomPadding()
```


## Exemples



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
