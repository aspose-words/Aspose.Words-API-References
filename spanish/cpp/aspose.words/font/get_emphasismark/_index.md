---
title: "Método Aspose::Words::Font::get_EmphasisMark"
linktitle: "get_EmphasisMark"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_EmphasisMark. Obtiene o establece la marca de énfasis aplicada a este formato en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


Obtiene o establece la marca de énfasis aplicada a este formato.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## Ejemplos



Muestra cómo agregar un carácter adicional renderizado encima/debajo del glyph-character.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Tipos posibles de marca de énfasis:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## Ver también

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
