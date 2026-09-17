---
title: "Méthode Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells. Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées par HorizontalMerge en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées par [HorizontalMerge](../../cellformat/get_horizontalmerge/).

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Remarques


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

Lorsque la cellule du tableau est fusionnée par la propriété de largeur, [HorizontalMerge](../../cellformat/get_horizontalmerge/) n'a aucun sens, mais parfois disposer de drapeaux de fusion est plus pratique.

Utilisez cette méthode pour transformer les cellules du tableau fusionnées horizontalement par largeur en cellules fusionnées par des drapeaux de fusion.

## Exemples



Montre comment convertir les cellules fusionnées horizontalement par largeur en cellules fusionnées par CellFormat.HorizontalMerge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word n'écrit plus les drapeaux de fusion, définissant les cellules fusionnées par largeur à la place.
// Aspose.Words définit par défaut uniquement 5 cellules par ligne, et aucune d'elles n'a le drapeau de fusion horizontal,
// bien qu'il y ait eu 7 cellules dans la ligne avant que la fusion horizontale n'ait eu lieu.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// Utilisez la méthode "ConvertToHorizontallyMergedCells" pour convertir les cellules fusionnées horizontalement
// par sa largeur vers la cellule fusionnée horizontalement par des indicateurs.
// Maintenant, nous avons 7 cellules, et certaines d'entre elles ont des valeurs de fusion horizontale.
table->ConvertToHorizontallyMergedCells();
row = table->get_Rows()->idx_get(0);

ASSERT_EQ(7, row->get_Cells()->get_Count());

ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(0)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(1)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(2)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(3)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(4)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(5)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(6)->get_CellFormat()->get_HorizontalMerge());
```

## Voir aussi

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
