---
title: "Método Aspose::Words::AbsolutePositionTab::Accept"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::AbsolutePositionTab::Accept. Acepta un visitante en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará el nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Observaciones


Llama a [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
