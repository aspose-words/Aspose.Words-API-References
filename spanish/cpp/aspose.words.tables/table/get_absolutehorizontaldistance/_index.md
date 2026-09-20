---
title: "Método Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance"
linktitle: "get_AbsoluteHorizontalDistance"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance. Obtiene o establece la posición horizontal absoluta de la tabla flotante especificada por las propiedades de la tabla, en puntos. El valor predeterminado es 0 en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.tables/table/get_absolutehorizontaldistance/
---
## Table::get_AbsoluteHorizontalDistance method


Obtiene o establece la posición horizontal absoluta de la tabla flotante especificada por las propiedades de la tabla, en puntos. El valor predeterminado es 0.

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance()
```


## Ejemplos



Muestra cómo establecer la ubicación de las tablas flotantes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Establece la ubicación de la tabla en un lugar de la página, como, en este caso, la esquina inferior derecha.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// También podemos establecer un desplazamiento horizontal y vertical en puntos desde la ubicación del párrafo donde insertamos la tabla.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
