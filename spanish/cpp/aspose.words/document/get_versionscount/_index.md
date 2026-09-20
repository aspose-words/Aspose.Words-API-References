---
title: "Método Aspose::Words::Document::get_VersionsCount"
linktitle: "get_VersionsCount"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_VersionsCount method. Obtiene el número de versiones del documento que se almacenaron en el documento DOC en C++."
type: docs
weight: 57000
url: /es/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


Obtiene el número de versiones del documento que se almacenó en el documento DOC.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Observaciones


Las versiones en Microsoft Word se acceden a través del menú Archivo/Versiones. Microsoft Word solo admite versiones para archivos DOC.

Esta propiedad permite detectar si había versiones del documento almacenadas en este documento antes de que se abriera en Aspose.Words. Aspose.Words no ofrece otro soporte para versiones de documentos. Si guarda este documento usando Aspose.Words, el documento se guardará sin versiones.

## Ejemplos



Muestra cómo trabajar con la función de recuento de versiones de documentos antiguos de Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// Podemos leer esta propiedad de un documento, pero no podemos preservarla al guardar.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
