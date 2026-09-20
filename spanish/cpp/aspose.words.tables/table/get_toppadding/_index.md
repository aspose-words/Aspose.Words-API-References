---
title: "Aspose::Words::Tables::Table::get_TopPadding método"
linktitle: "get_TopPadding"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::get_TopPadding método. Obtiene o establece la cantidad de espacio (en puntos) que se agrega encima del contenido de las celdas en C++."
type: docs
weight: 40000
url: /es/cpp/aspose.words.tables/table/get_toppadding/
---
## Table::get_TopPadding method


Obtiene o establece la cantidad de espacio (en puntos) que se agrega encima del contenido de las celdas.

```cpp
double Aspose::Words::Tables::Table::get_TopPadding()
```


## Ejemplos



Muestra cómo configurar el relleno de contenido en una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// Para cada celda de la tabla, establezca la distancia entre su contenido y cada uno de sus bordes.
// Esta tabla mantendrá la distancia mínima de relleno al ajustar el texto.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
