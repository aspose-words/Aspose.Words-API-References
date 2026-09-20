---
title: "Método Aspose::Words::Font::get_Shading"
linktitle: "get_Shading"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Shading. Devuelve un objeto Shading que se refiere al formato de sombreado para la fuente en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Devuelve un objeto [Shading](../../shading/) que se refiere al formato de sombreado para la fuente.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Ejemplos



Muestra cómo aplicar sombreado al texto creado por un generador de documentos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// Una forma de hacer visible el texto creado usando nuestro color de fuente blanco
// es aplicar un efecto de sombreado de fondo.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## Ver también

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
