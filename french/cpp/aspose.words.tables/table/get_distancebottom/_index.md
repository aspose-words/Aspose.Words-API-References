---
title: "Aspose::Words::Tables::Table::get_DistanceBottom méthode"
linktitle: "get_DistanceBottom"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_DistanceBottom méthode. Obtient ou définit la distance entre le bas du tableau et le texte environnant, en points en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.tables/table/get_distancebottom/
---
## Table::get_DistanceBottom method


Obtient ou définit la distance entre le bas du tableau et le texte environnant, en points.

```cpp
double Aspose::Words::Tables::Table::get_DistanceBottom()
```


## Exemples



Montre comment définir la distance entre les bordures du tableau et le texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Définir la distance entre le tableau et le texte environnant.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## Voir aussi

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
