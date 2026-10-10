---
title: "Aspose::Words::Tables::Table::get_DistanceBottom método"
linktitle: "get_DistanceBottom"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::get_DistanceBottom método. Obtiene o establece la distancia entre la parte inferior de la tabla y el texto circundante, en puntos en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.tables/table/get_distancebottom/
---
## Table::get_DistanceBottom method


Obtiene o establece la distancia entre la parte inferior de la tabla y el texto circundante, en puntos.

```cpp
double Aspose::Words::Tables::Table::get_DistanceBottom()
```


## Ejemplos



Muestra cómo establecer la distancia entre los bordes de la tabla y el texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Establecer la distancia entre la tabla y el texto circundante.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
