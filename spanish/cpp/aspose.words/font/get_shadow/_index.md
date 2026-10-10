---
title: "Método Aspose::Words::Font::get_Shadow"
linktitle: "get_Shadow"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Shadow. Verdadero si la fuente está formateada con sombra en C++."
type: docs
weight: 35000
url: /es/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


True si la fuente está formateada como sombreada.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Ejemplos



Muestra cómo crear una secuencia de texto formateada con sombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establezca el indicador Shadow para aplicar un efecto de sombra desplazada,
// haciendo que las letras parezcan flotar sobre la página.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
