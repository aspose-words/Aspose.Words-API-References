---
title: "Méthode get_StyleIdentifier de Aspose::Words::Tables::Table"
linktitle: "get_StyleIdentifier"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode get_StyleIdentifier de Aspose::Words::Tables::Table. Obtient ou définit l'identifiant de style indépendant de la locale du style de tableau appliqué à ce tableau en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words.tables/table/get_styleidentifier/
---
## Table::get_StyleIdentifier method


Obtient ou définit l'identifiant de style indépendant de la locale du style de tableau appliqué à ce tableau.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Tables::Table::get_StyleIdentifier()
```


## Exemples



Montre comment créer un nouveau tableau tout en appliquant un style.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Nous devons insérer au moins une ligne avant de définir tout format de tableau.
builder->InsertCell();

// Définissez le style de tableau utilisé en fonction de l'identifiant du style.
// Notez que tous les styles de tableau ne sont pas disponibles lors de l'enregistrement au format .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Appliquez partiellement le style aux caractéristiques du tableau en fonction des prédicats, puis construisez le tableau.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## Voir aussi

* Enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
