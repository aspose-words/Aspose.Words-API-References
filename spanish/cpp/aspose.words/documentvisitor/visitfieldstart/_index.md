---
title: "Método Aspose::Words::DocumentVisitor::VisitFieldStart"
linktitle: "VisitFieldStart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentVisitor::VisitFieldStart. Llamado cuando un campo comienza en el documento en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Se llama cuando comienza un campo en el documento.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | El objeto que está siendo visitado. |

### ReturnValue

Un valor [VisitorAction](../../visitoraction/) que especifica cómo continuar la enumeración.
## Observaciones


Un campo en un documento Word consta de un código de campo y un valor de campo.

Por ejemplo, un campo que muestra un número de página puede representarse de la siguiente manera:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

El separador de campos separa el código de campo del valor de campo en el documento. Nota que algunos campos solo tienen código de campo y no tienen separador de campo ni valor de campo.

[Fields](../../../aspose.words.fields/) can be nested.

## Ver también

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
