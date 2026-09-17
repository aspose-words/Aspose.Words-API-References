---
title: "Aspose::Words::Tables::Cell::get_CellFormat méthode"
linktitle: "get_CellFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Cell::get_CellFormat méthode. Fournit l'accès aux propriétés de mise en forme de la cellule en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.tables/cell/get_cellformat/
---
## Cell::get_CellFormat method


Fournit l'accès aux propriétés de mise en forme de la cellule.

```cpp
System::SharedPtr<Aspose::Words::Tables::CellFormat> Aspose::Words::Tables::Cell::get_CellFormat()
```


## Exemples



Montre comment modifier le format des lignes et des cellules d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Utilisez la propriété "RowFormat" de la première ligne pour modifier le formatage
// du contenu de toutes les cellules de cette ligne.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Utilisez la propriété "CellFormat" de la première cellule de la dernière ligne pour modifier le formatage du contenu de cette cellule.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Montre comment modifier le formatage d'une cellule de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Utilisez la propriété "CellFormat" d'une cellule pour définir le formatage qui modifie l'apparence de cette cellule.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```


Montre comment combiner les lignes de deux tables en une seule.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Voici deux façons d'obtenir une table à partir d'un document.
// 1 -  À partir de la collection "Tables" d'un nœud Body :
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  En utilisant la méthode "GetChild" :
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Ajoutez toutes les lignes de la table actuelle à la suivante.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Supprimez le conteneur de table vide.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Voir aussi

* Class [CellFormat](../../cellformat/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
