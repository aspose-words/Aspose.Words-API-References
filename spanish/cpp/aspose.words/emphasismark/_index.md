---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::EmphasisMark enum. Especifica los tipos posibles de marca de énfasis en C++."
type: docs
weight: 89000
url: /es/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Especifica los tipos posibles de marca de énfasis.

```cpp
enum class EmphasisMark
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Sin marca de énfasis. |
| OverSolidCircle | 1 | La marca de énfasis es un círculo negro sólido que se muestra encima del texto. |
| OverComma | 2 | La marca de énfasis es un carácter de coma que se muestra encima del texto. |
| OverWhiteCircle | 3 | La marca de énfasis es un círculo blanco vacío que se muestra encima del texto. |
| UnderSolidCircle | 4 | La marca de énfasis es un círculo negro sólido que se muestra debajo del texto. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
