---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps método"
linktitle: "get_HyphenateCaps"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps método. Obtiene o establece el valor que determina si las palabras escritas en mayúsculas se dividen con guiones. El valor predeterminado para esta propiedad es true en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


Obtiene o establece el valor que determina si las palabras escritas en mayúsculas se dividen con guiones. El valor predeterminado para esta propiedad es **true**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
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
