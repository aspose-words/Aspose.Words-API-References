---
title: "Aspose::Words::Tables::TableStyleOptions enum"
linktitle: "TableStyleOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::TableStyleOptions enum. Spécifie comment le style de tableau est appliqué à un tableau en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Spécifie comment le style de tableau est appliqué à un tableau.

```cpp
enum class TableStyleOptions
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucun format de style de tableau n'est appliqué. |
| FirstRow | 32 | Appliquer le format conditionnel à la première ligne. |
| LastRow | 64 | Appliquer le format conditionnel à la dernière ligne. |
| FirstColumn | 128 | Appliquer le format conditionnel à la première colonne 1. |
| LastColumn | 256 | Appliquer le format conditionnel à la dernière colonne. |
| RowBands | 512 | Appliquer le format conditionnel de bandes de lignes. |
| ColumnBands | 1024 | Appliquer le format conditionnel de bandes de colonnes. |
| Default2003 | n/a | [Row](../row/) et les bandes de colonnes sont appliquées. C’est le comportement par défaut de Microsoft Word pour les anciens formats tels que DOC, WML et RTF. |
| Default | n/a | Ceci est le comportement par défaut de Microsoft Word. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
