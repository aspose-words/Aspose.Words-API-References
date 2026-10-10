---
title: "Método Aspose::Words::Font::get_Kerning"
linktitle: "get_Kerning"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Kerning. Obtiene o establece el tamaño de fuente en el que comienza el kerning en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Obtiene o establece el tamaño de fuente a partir del cual comienza el kerning.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Ejemplos



Muestra cómo especificar el tamaño de fuente en el que el kerning comienza a tener efecto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Establezca el tamaño de fuente del generador y el tamaño mínimo en el que el kerning tendrá efecto.
// El tamaño de fuente cae por debajo del umbral de kerning, por lo que la ejecución siguiente no tendrá kerning.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Establezca el umbral de kerning para que el tamaño de fuente actual del generador esté por encima de él.
// Cualquier texto que agreguemos a partir de este punto tendrá kerning aplicado. Los espacios entre caracteres
// serán ajustados, normalmente resultando en un segmento de texto ligeramente más estético.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
