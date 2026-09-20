---
title: "Método Aspose::Words::EditableRangeEnd::Accept"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::EditableRangeEnd::Accept. Acepta un visitante en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/editablerangeend/accept/
---
## EditableRangeEnd::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::EditableRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará el nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Observaciones


Llama a [VisitEditableRangeEnd()](../../documentvisitor/visiteditablerangeend/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
