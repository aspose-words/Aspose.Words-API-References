---
title: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes método"
linktitle: "GetChildNodes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes método. Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado en C++."
type: docs
weight: 34500
url: /es/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Especifica el tipo de nodos a seleccionar. |
| isDeep | bool | **true** para seleccionar de todos los nodos hijos de forma recursiva; **false** para seleccionar solo entre los hijos inmediatos. |

### ReturnValue

Una colección en vivo de nodos hijos del tipo especificado.
## Observaciones


La colección de nodos devuelta por este método está siempre en vivo.

Una colección en vivo siempre está sincronizada con el documento. Por ejemplo, si seleccionas todas las secciones de un documento y recorres la colección eliminando las secciones, la sección se elimina de la colección inmediatamente cuando se elimina del documento.

## Ver también

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
