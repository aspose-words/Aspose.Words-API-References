---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing méthode"
linktitle: "get_AllowCellSpacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing méthode. Obtient ou définit l'option \"Autoriser l'espacement entre les cellules\" en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


Obtient ou définit l'option "Allow spacing between cells".

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Exemples



Montre comment activer l'espacement entre les cellules individuelles d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Définissez la propriété "AllowCellSpacing" sur "true" pour activer l'espacement entre les cellules
// avec une magnitude égale à la valeur de la propriété "CellSpacing", en points.
// Définissez la propriété "AllowCellSpacing" sur "false" pour désactiver l'espacement des cellules
// et ignorez la valeur de la propriété "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Modifier la propriété "CellSpacing" activera automatiquement l'espacement des cellules.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## Voir aussi

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
