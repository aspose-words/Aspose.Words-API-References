---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences method"
linktitle: "RemoveExternalSchemaReferences"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences method. Elimina referencias externas a esquemas XML de este documento en C++."
type: docs
weight: 68000
url: /es/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


Elimina referencias externas de esquemas XML de este documento.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## Ejemplos



Muestra cómo eliminar todas las referencias externas a esquemas XML de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
