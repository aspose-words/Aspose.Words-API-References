---
title: "Método Aspose::Words::SpecialChar::Accept"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::SpecialChar::Accept. Acepta un visitante en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/specialchar/accept/
---
## SpecialChar::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::SpecialChar::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará el nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Observaciones


Llama a [VisitSpecialChar()](../../documentvisitor/visitspecialchar/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../documentvisitor/)
* Class [SpecialChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
