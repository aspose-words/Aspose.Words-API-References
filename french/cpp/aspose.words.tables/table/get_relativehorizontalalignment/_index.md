---
title: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment méthode"
linktitle: "get_RelativeHorizontalAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment méthode. Obtient ou définit l'alignement horizontal relatif du tableau flottant en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words.tables/table/get_relativehorizontalalignment/
---
## Table::get_RelativeHorizontalAlignment method


Obtient ou définit l'alignement horizontal relatif du tableau flottant.

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment()
```


## Exemples



Montre comment définir l'emplacement des tableaux flottants.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Définissez l'emplacement du tableau à un endroit de la page, comme, dans ce cas, le coin inférieur droit.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Nous pouvons également définir un décalage horizontal et vertical en points à partir de l'emplacement du paragraphe où nous avons inséré le tableau.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## Voir aussi

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
