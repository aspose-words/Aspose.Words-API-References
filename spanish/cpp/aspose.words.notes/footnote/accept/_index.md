---
title: "Aspose::Words::Notes::Footnote::Accept method"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::Footnote::Accept method. Acepta un visitante en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.notes/footnote/accept/
---
## Footnote::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::Notes::Footnote::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará los nodos. |

### ReturnValue

Verdadero si se visitaron todos los nodos; falso si [DocumentVisitor](../../../aspose.words/documentvisitor/) detuvo la operación antes de visitar todos los nodos.
## Observaciones


Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en [DocumentVisitor](../../../aspose.words/documentvisitor/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
