---
title: "Método Aspose::Words::Document::get_JustificationMode"
linktitle: "get_JustificationMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_JustificationMode. Obtiene o establece el ajuste de espaciado de caracteres de un documento en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Obtiene o establece el ajuste de espaciado de caracteres de un documento.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


## Ejemplos



Muestra cómo gestionar el control del espaciado de caracteres.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Ver también

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
