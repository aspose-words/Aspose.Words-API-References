---
title: "Méthode Aspose::Words::Tables::Table::get_StyleOptions"
linktitle: "get_StyleOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_StyleOptions méthode. Obtient ou définit les indicateurs binaires qui spécifient comment un style de tableau est appliqué à cette table en C++."
type: docs
weight: 37000
url: /fr/cpp/aspose.words.tables/table/get_styleoptions/
---
## Table::get_StyleOptions method


Obtient ou définit les indicateurs binaires qui spécifient comment un style de tableau est appliqué à ce tableau.

```cpp
Aspose::Words::Tables::TableStyleOptions Aspose::Words::Tables::Table::get_StyleOptions()
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

* Enum [TableStyleOptions](../../tablestyleoptions/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
