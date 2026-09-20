---
title: "Aspose::Words::Tables::TextWrapping enum"
linktitle: "TextWrapping"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::TextWrapping enum. Especifica cómo se envuelve el texto alrededor de la tabla en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


Especifica cómo se ajusta el texto alrededor de la tabla.

```cpp
enum class TextWrapping
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | El texto y la tabla se muestran en el orden de su aparición en el documento. |
| Alrededor | 1 | El texto se envuelve alrededor de la tabla ocupando el espacio lateral disponible. |
| Predeterminado | n/a | Valor predeterminado. |


## Ejemplos



Muestra cómo trabajar con el ajuste de texto de la tabla.
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

// Establece la propiedad "TextWrapping" a "TextWrapping.Around" para que la tabla envuelva el texto a su alrededor,
// y empújalo hacia abajo en el párrafo siguiente estableciendo la posición.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Ver también

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
