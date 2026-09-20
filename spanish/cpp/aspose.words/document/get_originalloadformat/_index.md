---
title: "Aspose::Words::Document::get_OriginalLoadFormat método"
linktitle: "get_OriginalLoadFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_OriginalLoadFormat método. Obtiene el formato del documento original que se cargó en este objeto en C++."
type: docs
weight: 41000
url: /es/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Obtiene el formato del documento original que se cargó en este objeto.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Observaciones


Si creó un documento nuevo en blanco, devuelve el valor [Doc](../../loadformat/).

## Ejemplos



Muestra cómo obtener los detalles de la operación de carga de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## Ver también

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
