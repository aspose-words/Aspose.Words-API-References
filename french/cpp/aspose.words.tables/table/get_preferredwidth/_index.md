---
title: "Aspose::Words::Tables::Table::get_PreferredWidth méthode"
linktitle: "get_PreferredWidth"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_PreferredWidth méthode. Obtient ou définit la largeur préférée du tableau en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Obtient ou définit la largeur préférée du tableau.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Remarques


La valeur par défaut est [Auto](../../preferredwidth/auto/).

## Exemples



Montre comment régler une table pour qu'elle s'ajuste automatiquement à 50 % de la largeur de la page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## Voir aussi

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
