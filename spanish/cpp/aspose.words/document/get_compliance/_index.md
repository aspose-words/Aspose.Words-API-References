---
title: "Método Aspose::Words::Document::get_Compliance"
linktitle: "get_Compliance"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_Compliance. Obtiene la versión de cumplimiento OOXML determinada a partir del contenido del documento cargado. Solo tiene sentido para documentos OOXML en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Obtiene la versión de cumplimiento OOXML determinada a partir del contenido del documento cargado. Solo tiene sentido para documentos OOXML.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Observaciones


Si creó un documento nuevo en blanco o cargó un documento que no es OOXML, devuelve el valor [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Ejemplos



Muestra cómo leer la versión de cumplimiento Open Office XML de un documento cargado.
```cpp
// La versión de cumplimiento varía entre documentos creados por diferentes versiones de Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## Ver también

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
