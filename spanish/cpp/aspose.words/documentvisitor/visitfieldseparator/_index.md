---
title: "Aspose::Words::DocumentVisitor::VisitFieldSeparator method"
linktitle: "VisitFieldSeparator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentVisitor::VisitFieldSeparator method. Llamado cuando se encuentra un separador de campo en el documento en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


Se llama cuando se encuentra un separador de campo en el documento.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | El objeto que está siendo visitado. |

### ReturnValue

Un valor [VisitorAction](../../visitoraction/) que especifica cómo continuar la enumeración.
## Observaciones


El separador de campos separa el código de campo del valor de campo en el documento. Nota que algunos campos solo tienen código de campo y no tienen separador de campo ni valor de campo.

Para más información, consulte [VisitFieldStart()](../visitfieldstart/)

## Ver también

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
