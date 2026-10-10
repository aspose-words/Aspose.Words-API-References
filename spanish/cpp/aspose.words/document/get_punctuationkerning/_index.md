---
title: "Método Aspose::Words::Document::get_PunctuationKerning"
linktitle: "get_PunctuationKerning"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_PunctuationKerning. Especifica si el kerning se aplica tanto al texto latino como a la puntuación en C++."
type: docs
weight: 44500
url: /es/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Especifica si el kerning se aplica tanto al texto latino como a la puntuación.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Ejemplos



Muestra cómo trabajar con kerning que se aplica tanto al texto latino como a la puntuación.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
