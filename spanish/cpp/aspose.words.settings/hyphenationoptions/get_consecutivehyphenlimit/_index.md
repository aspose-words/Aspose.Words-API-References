---
title: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit método"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit método. Obtiene o establece el número máximo de líneas consecutivas que pueden terminar con guiones. El valor predeterminado para esta propiedad es 0 en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Obtiene o establece el número máximo de líneas consecutivas que pueden terminar con guiones. El valor predeterminado para esta propiedad es 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Observaciones


Si el valor de esta propiedad se establece en 0, cualquier número de líneas consecutivas puede terminar con guiones.

La propiedad no tiene efecto al guardar en formatos de página fija, p. ej., PDF.

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
