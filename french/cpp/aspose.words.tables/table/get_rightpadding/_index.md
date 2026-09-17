---
title: "Aspose::Words::Tables::Table::get_RightPadding méthode"
linktitle: "get_RightPadding"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_RightPadding méthode. Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words.tables/table/get_rightpadding/
---
## Table::get_RightPadding method


Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules.

```cpp
double Aspose::Words::Tables::Table::get_RightPadding()
```


## Exemples



Montre comment configurer le remplissage du contenu dans un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// Pour chaque cellule du tableau, définissez la distance entre son contenu et chacune de ses bordures.
// Ce tableau maintiendra la distance minimale de remplissage en ajustant le texte.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Voir aussi

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
