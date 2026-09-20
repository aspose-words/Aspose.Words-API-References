---
title: "Método Aspose::Words::Font::get_Emboss"
linktitle: "get_Emboss"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Emboss. Verdadero si la fuente está formateada como relieve en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/font/get_emboss/
---
## Font::get_Emboss method


Verdadero si la fuente está formateada como relieve.

```cpp
bool Aspose::Words::Font::get_Emboss()
```


## Ejemplos



Muestra cómo aplicar efectos de grabado/relieve al texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// A continuación se presentan dos formas de usar sombras para aplicar un efecto similar a 3D al texto.
// 1 -  Grabar texto para que parezca que las letras están hundidas en la página:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Aplicar relieve al texto para que parezca que las letras sobresalen de la página:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
