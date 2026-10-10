---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge méthode"
linktitle: "get_VerticalMerge"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge méthode. Spécifie comment la cellule est fusionnée avec d'autres cellules verticalement en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Spécifie comment la cellule est fusionnée avec d'autres cellules verticalement.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Remarques


Les cellules ne peuvent être fusionnées verticalement que si leurs limites gauche et droite sont identiques.

Lorsque les cellules sont fusionnées verticalement, les zones d'affichage des cellules fusionnées sont consolidées. La zone consolidée est utilisée pour afficher le contenu de la première cellule fusionnée verticalement et toutes les autres cellules fusionnées verticalement doivent être vides.

## Exemples



Montre comment fusionner les cellules d'un tableau verticalement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une cellule dans la première colonne de la première ligne.
// Cette cellule sera la première d'une plage de cellules fusionnées verticalement.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Insérez une cellule dans la deuxième colonne de la première ligne, puis terminez la ligne.
// De plus, configurez le constructeur pour désactiver la fusion verticale dans les cellules créées.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Insérez une cellule dans la première colonne de la deuxième ligne.
// Au lieu d'ajouter du texte, nous allons fusionner cette cellule avec la première cellule que nous avons ajoutée directement au-dessus.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Insérez une autre cellule indépendante dans la deuxième colonne de la deuxième ligne.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```

## Voir aussi

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
