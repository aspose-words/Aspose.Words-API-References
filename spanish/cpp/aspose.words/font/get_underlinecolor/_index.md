---
title: "Método Aspose::Words::Font::get_UnderlineColor"
linktitle: "get_UnderlineColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_UnderlineColor. Obtiene o establece el color del subrayado aplicado a la fuente en C++."
type: docs
weight: 56000
url: /es/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Obtiene o establece el color del subrayado aplicado a la fuente.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Ejemplos



Muestra cómo configurar el estilo y el color de un subrayado de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
