---
title: "Método Aspose::Words::Font::get_Outline"
linktitle: "get_Outline"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Outline. Verdadero si la fuente está formateada como contorno en C++."
type: docs
weight: 31000
url: /es/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


True si la fuente está formateada como contorno.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Ejemplos



Muestra cómo crear una secuencia de texto formateada como contorno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establezca la bandera Outline para cambiar el color de relleno del texto a blanco y
// dejar un contorno fino alrededor de cada carácter con el color original del texto.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
