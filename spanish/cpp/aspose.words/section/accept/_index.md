---
title: "Método Aspose::Words::Section::Accept"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Section::Accept. Acepta un visitante en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/section/accept/
---
## Section::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::Section::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará los nodos. |

### ReturnValue

Verdadero si se visitaron todos los nodos; falso si [DocumentVisitor](../../documentvisitor/) detuvo la operación antes de visitar todos los nodos.
## Observaciones


Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en [DocumentVisitor](../../documentvisitor/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
