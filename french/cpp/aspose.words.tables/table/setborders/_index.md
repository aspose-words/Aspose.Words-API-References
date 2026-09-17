---
title: "Méthode Aspose::Words::Tables::Table::SetBorders"
linktitle: "SetBorders"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::Table::SetBorders. Définit toutes les bordures du tableau avec le style de ligne, la largeur et la couleur spécifiés en C++."
type: docs
weight: 69000
url: /fr/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Définit toutes les bordures du tableau avec le style de ligne, la largeur et la couleur spécifiés.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | Le style de ligne à appliquer. |
| lineWidth | double | La largeur de ligne à définir (en points). |
| color | System::Drawing::Color | La couleur à utiliser pour la bordure. |

## Exemples



Montre comment appliquer la couleur de bordure et d’ombrage lors de la création d’une table.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Démarrez une table et définissez une couleur/épaisseur par défaut pour ses bordures.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Créez une ligne avec deux cellules ayant des couleurs d’arrière-plan différentes.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Réinitialisez le formatage des cellules pour désactiver les couleurs d’arrière-plan
// définissez une épaisseur de bordure personnalisée pour toutes les nouvelles cellules créées par le constructeur,
// puis construisez une deuxième ligne.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Montre comment formater toutes les bordures d'un tableau en une fois.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Supprime toutes les bordures existantes du tableau.
table->ClearBorders();

// Définit une seule ligne verte comme bordure extérieure et intérieure de ce tableau.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## Voir aussi

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
