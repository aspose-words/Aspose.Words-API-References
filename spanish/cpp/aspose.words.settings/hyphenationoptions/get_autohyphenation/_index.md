---
title: "Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation método"
linktitle: "get_AutoHyphenation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation método. Obtiene o establece el valor que determina si la hyphenación automática está activada para el documento. El valor predeterminado para esta propiedad es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.settings/hyphenationoptions/get_autohyphenation/
---
## HyphenationOptions::get_AutoHyphenation method


Obtiene o establece el valor que determina si el guionado automático está activado para el documento. El valor predeterminado de esta propiedad es **false**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation() const
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
