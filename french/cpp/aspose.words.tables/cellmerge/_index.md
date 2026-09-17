---
title: "Énumération Aspose::Words::Tables::CellMerge"
linktitle: "CellMerge"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Tables::CellMerge. Spécifie comment une cellule d'un tableau est fusionnée avec d'autres cellules en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Spécifie comment une cellule d'un tableau est fusionnée avec d'autres cellules.

```cpp
enum class CellMerge
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | La cellule n'est pas fusionnée. |
| First | 1 | La cellule est la première cellule d'une plage de cellules fusionnées. |
| Précédent | 2 | La cellule est fusionnée à la cellule précédente horizontalement ou verticalement. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
