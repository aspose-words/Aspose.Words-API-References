---
title: "Aspose::Words::DocumentBuilder::InsertCell method"
linktitle: "InsertCell"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertCell method. Insère une cellule de tableau dans le document en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder::InsertCell method


Insère une cellule de tableau dans le document.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::DocumentBuilder::InsertCell()
```


### ReturnValue

Le nœud de cellule qui vient d'être inséré.
## Remarques


Pour démarrer un tableau, appelez simplement [InsertCell](./). Après cela, tout contenu que vous ajoutez en utilisant d'autres méthodes de la classe [DocumentBuilder](../) sera ajouté à la cellule actuelle.

Pour démarrer une nouvelle cellule dans la même ligne, appelez à nouveau [InsertCell](./).

Pour terminer une ligne de tableau, appelez [EndRow](../endrow/).

Utilisez la propriété [CellFormat](../get_cellformat/) pour spécifier le formatage des cellules.

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


Montre comment utiliser un DocumentBuilder pour créer un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Démarrez le tableau, puis remplissez la première ligne avec deux cellules.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Appelez la méthode "EndRow" du constructeur pour démarrer une nouvelle ligne.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Voir aussi

* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
