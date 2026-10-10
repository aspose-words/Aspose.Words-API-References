---
title: "Aspose::Words::Tables::Table::get_TextWrapping méthode"
linktitle: "get_TextWrapping"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_TextWrapping méthode. Obtient ou définit TextWrapping pour le tableau en C++."
type: docs
weight: 38000
url: /fr/cpp/aspose.words.tables/table/get_textwrapping/
---
## Table::get_TextWrapping method


Obtient ou définit [TextWrapping](./) pour le tableau.

```cpp
Aspose::Words::Tables::TextWrapping Aspose::Words::Tables::Table::get_TextWrapping()
```


## Exemples



Montre comment travailler avec l'enveloppement du texte de la table.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Définissez la propriété "TextWrapping" sur "TextWrapping.Around" pour que la table enveloppe le texte autour d'elle,
// et poussez-le vers le bas dans le paragraphe suivant en définissant la position.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Voir aussi

* Enum [TextWrapping](../../textwrapping/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
