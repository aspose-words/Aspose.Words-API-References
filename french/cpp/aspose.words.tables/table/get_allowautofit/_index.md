---
title: "Méthode Aspose::Words::Tables::Table::get_AllowAutoFit"
linktitle: "get_AllowAutoFit"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::Table::get_AllowAutoFit. Permet à Microsoft Word et à Aspose.Words de redimensionner automatiquement les cellules d'un tableau pour adapter leur contenu en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Permet à Microsoft Word et à Aspose.Words de redimensionner automatiquement les cellules d'un tableau pour qu'elles s'adaptent à leur contenu.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Remarques


La valeur par défaut est **true**.

## Exemples



Montre comment activer/désactiver le redimensionnement automatique des cellules de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Définissez la propriété "AllowAutoFit" sur "false" pour que le tableau conserve les dimensions
// de toutes ses lignes et cellules, et tronquez le contenu s'il devient trop volumineux pour tenir.
// Définissez la propriété "AllowAutoFit" sur "true" pour permettre au tableau de modifier la largeur et la hauteur de ses cellules
// afin d'accueillir leur contenu.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## Voir aussi

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
