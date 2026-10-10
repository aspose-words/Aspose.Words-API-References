---
title: "Aspose::Words::Tables::CellFormat::SetPaddings método"
linktitle: "SetPaddings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::CellFormat::SetPaddings método. Establece la cantidad de espacio (en puntos) que se agrega a la izquierda/arriba/derecha/abajo del contenido de la celda en C++."
type: docs
weight: 31000
url: /es/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Establece la cantidad de espacio (en puntos) que se añadirá a la izquierda/arriba/derecha/abajo del contenido de la celda.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Ejemplos



Muestra cómo rellenar el contenido de una celda con espacios en blanco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establezca una distancia de relleno (en puntos) entre el borde y el contenido del texto
// de cada celda de tabla que creamos con el generador de documentos.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// Cree una tabla con una celda cuyo contenido tendrá relleno de espacios en blanco.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## Ver también

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
