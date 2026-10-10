---
title: "Método Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine"
linktitle: "get_MaxCharactersPerLine"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine. Obtiene o establece un valor entero que especifica el número máximo de caracteres por línea. El valor predeterminado es 0, lo que significa sin límite en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Obtiene o establece un valor entero que especifica el número máximo de caracteres por línea. El valor predeterminado es 0, lo que significa sin límite.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Ejemplos



Muestra cómo establecer el número máximo de caracteres por línea.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Establezca 30 caracteres como máximo permitido por línea.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## Ver también

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
