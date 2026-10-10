---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop método"
linktitle: "get_LinesToDrop"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop método. Obtiene o establece el número de líneas del texto del párrafo usadas para calcular la altura de la letra capitular en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Obtiene o establece el número de líneas del texto del párrafo usadas para calcular la altura de la inicial mayúscula.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Ejemplos



Muestra cómo establecer el tamaño de una letra capitular.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifique la propiedad "LinesToDrop" para designar un párrafo como letra capitular,
// lo que lo convertirá en una letra mayúscula grande que decorará el siguiente párrafo.
// Asigne a esta propiedad el valor 4 para dar a la letra capitular la altura de cuatro líneas de texto.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// Restablezca la propiedad "LinesToDrop" a 0 para convertir el siguiente párrafo en un párrafo ordinario.
// El texto en este párrafo se ajustará alrededor de la letra capitular.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
