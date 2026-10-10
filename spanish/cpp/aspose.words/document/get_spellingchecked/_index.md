---
title: "Método Aspose::Words::Document::get_SpellingChecked"
linktitle: "get_SpellingChecked"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_SpellingChecked. Devuelve true si el documento ha sido revisado ortográficamente en C++."
type: docs
weight: 52000
url: /es/cpp/aspose.words/document/get_spellingchecked/
---
## Document::get_SpellingChecked method


Devuelve **true** si el documento ha sido revisado ortográficamente.

```cpp
bool Aspose::Words::Document::get_SpellingChecked()
```


## Ejemplos



Muestra cómo establecer la verificación ortográfica o gramatical.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// La cadena con errores ortográficos.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// La verificación ortográfica/gramatical comienza si establecemos las propiedades en false.
// Podemos ver todos los errores en Microsoft Word a través de Revisar -> Ortografía y gramática.
// Tenga en cuenta que Microsoft Word no inicia la revisión gramatical/ortográfica automáticamente para los formatos de documento DOC y RTF.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
