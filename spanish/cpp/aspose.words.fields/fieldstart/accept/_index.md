---
title: "Aspose::Words::Fields::FieldStart::Accept método"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldStart::Accept método. Acepta un visitante en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará el nodo. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Observaciones


Llama a [VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
