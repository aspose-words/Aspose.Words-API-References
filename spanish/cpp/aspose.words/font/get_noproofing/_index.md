---
title: "Aspose::Words::Font::get_NoProofing método"
linktitle: "get_NoProofing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_NoProofing método. Verdadero cuando los caracteres formateados no deben ser revisados ortográficamente en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


True cuando los caracteres formateados no deben revisarse ortográficamente.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Ejemplos



Muestra cómo evitar que el texto sea revisado ortográficamente por Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normalmente, Microsoft Word enfatiza los errores ortográficos con un subrayado rojo irregular.
// Podemos desactivar la bandera "NoProofing" para crear una porción de texto que
// eluda el corrector ortográfico mientras lo desactiva por completo.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
