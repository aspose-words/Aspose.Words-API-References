---
title: "Aspose::Words::Fields::FieldEnd::Accept método"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldEnd::Accept método. Acepta un visitante en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldend/accept/
---
## FieldEnd::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::Fields::FieldEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará el nodo. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Observaciones


Llama a [VisitFieldEnd()](../../../aspose.words/documentvisitor/visitfieldend/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldEnd](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
