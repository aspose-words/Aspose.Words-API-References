---
title: "Método Aspose::Words::Document::get_ShowSpellingErrors"
linktitle: "get_ShowSpellingErrors"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_ShowSpellingErrors. Especifica si se deben mostrar los errores ortográficos en este documento en C++."
type: docs
weight: 51000
url: /es/cpp/aspose.words/document/get_showspellingerrors/
---
## Document::get_ShowSpellingErrors method


Especifica si se muestran los errores ortográficos en este documento.

```cpp
bool Aspose::Words::Document::get_ShowSpellingErrors()
```


## Ejemplos



Muestra cómo mostrar/ocultar errores en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte dos oraciones con errores que serían detectados
// por los correctores ortográficos y gramaticales de Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// Si estas opciones están habilitadas, los errores ortográficos se subrayarán
// en el documento de salida con una línea roja irregular, y una línea azul doble resaltará los errores gramaticales.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
