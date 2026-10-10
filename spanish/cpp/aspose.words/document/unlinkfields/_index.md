---
title: "Aspose::Words::Document::UnlinkFields method"
linktitle: "UnlinkFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::UnlinkFields method. Desvincula los campos en todo el documento en C++."
type: docs
weight: 94000
url: /es/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Desvincula los campos en todo el documento.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Observaciones


Reemplaza todos los campos en todo el documento con sus resultados más recientes.

Para desvincular campos en una parte específica del documento, usa [UnlinkFields](../../range/unlinkfields/).

## Ejemplos



Muestra cómo desvincular todos los campos en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
