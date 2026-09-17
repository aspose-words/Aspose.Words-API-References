---
title: "Aspose::Words::BorderCollection::get_Bottom méthode"
linktitle: "get_Bottom"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection::get_Bottom méthode. Obtient la bordure inférieure en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/bordercollection/get_bottom/
---
## BorderCollection::get_Bottom method


Obtient la bordure inférieure.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Bottom()
```


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

## Voir aussi

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
