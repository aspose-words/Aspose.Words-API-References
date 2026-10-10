---
title: "Aspose::Words::Document::get_GrammarChecked método"
linktitle: "get_GrammarChecked"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_GrammarChecked método. Devuelve true si el documento ha sido revisado gramaticalmente en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words/document/get_grammarchecked/
---
## Document::get_GrammarChecked method


Devuelve **true** si el documento ha sido revisado por gramática.

```cpp
bool Aspose::Words::Document::get_GrammarChecked()
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
