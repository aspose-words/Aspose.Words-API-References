---
title: "Método Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone"
linktitle: "get_HyphenationZone"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone. Obtiene o establece la distancia en 1/20 de punto desde el margen derecho dentro de la cual no se desea dividir palabras con guión. El valor predeterminado para esta propiedad es 360 (0,25 pulgadas) en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


Obtiene o establece la distancia en 1/20 de punto desde el margen derecho dentro de la cual no se desea dividir palabras con guiones. El valor predeterminado para esta propiedad es 360 (0,25 pulgadas).

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
```


## Ejemplos



Muestra cómo configurar la división automática de palabras.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## Ver también

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
