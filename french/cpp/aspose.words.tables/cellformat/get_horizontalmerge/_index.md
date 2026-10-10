---
title: "Méthode Aspose::Words::Tables::CellFormat::get_HorizontalMerge"
linktitle: "get_HorizontalMerge"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::CellFormat::get_HorizontalMerge. Spécifie comment la cellule est fusionnée horizontalement avec d'autres cellules de la ligne en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Spécifie comment la cellule est fusionnée horizontalement avec d'autres cellules de la ligne.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Exemples



Montre comment fusionner les cellules d'un tableau horizontalement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une cellule dans la première colonne de la première ligne.
// Cette cellule sera la première d'une plage de cellules fusionnées horizontalement.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Insérez une cellule dans la deuxième colonne de la première ligne. Au lieu d'ajouter du texte,
// nous allons fusionner cette cellule avec la première cellule que nous avons ajoutée directement à gauche.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// Insérez deux cellules supplémentaires non fusionnées dans la deuxième ligne.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## Voir aussi

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
